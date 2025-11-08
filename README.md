# Something-Something-V2 Paraphrased Captions Dataset

## Overview

This dataset contains paraphrased captions for the Something-Something-V2 (https://cv.gluon.ai/build/examples_datasets/somethingsomethingv2.html) training set, generated to provide diverse caption variations while maintaining semantic consistency with the original annotations.I can generate paraphrases for validation too if there's interest.

## Statistics

### Coverage
- **Total videos in SSv2 training set**: 168,913
- **Videos with paraphrases**: 168,911
- **Coverage**: 100.0%

### Paraphrases per Video
- **Minimum**: 2
- **Maximum**: 21
- **Average**: 14.3
- **Median**: 14
- **Total paraphrases generated**: 2,422,755

### Caption Length (in words)

**Original Captions:**
- Min: 2 words
- Max: 31 words
- Average: 6.6 words
- Median: 6 words

**Paraphrased Captions:**
- Min: 1 words
- Max: 38 words
- Average: 11.0 words
- Median: 11 words

### Vocabulary Diversity
- **Original unique words**: 8,173
- **Paraphrase unique words**: 31,337
- **New words introduced**: 25,140

## Data Format

The paraphrases are stored in `ssv2_paraphrase.json` with the following structure:

```json
{
  "video_id": [
    "paraphrase 1",
    "paraphrase 2",
    ...
  ]
}
```

## Sample Examples

Here are some examples showing original captions and their paraphrases:


### Example 1

**Original**: holding potato next to vicks vaporub bottle

**Paraphrases**:
1. A hand presents a potato near a container of Vicks VapoRub.
2. The video shows a potato being held in close proximity to a Vicks VapoRub bottle.
3. A person is positioning a potato beside a bottle of Vicks VapoRub.
4. The scene depicts a potato held next to a Vicks VapoRub bottle.
5. A potato is held up, with a Vicks VapoRub bottle clearly visible nearby.
   _(and 9 more)_

### Example 2

**Original**: moving color pencils up

**Paraphrases**:
1. The colored pencils are being lifted upwards.
2. An upward motion is applied to the collection of colored pencils.
3. The color pencils are raised.
4. The colored pencils are going up.
5. The pencils are moved in an upward direction.
   _(and 9 more)_

### Example 3

**Original**: putting pen on a surface

**Paraphrases**:
1. The pen is being placed down onto a flat area.
2. A writing instrument is set down on a table.
3. The pen makes contact with the surface as it is lowered.
4. The action involves positioning a pen onto a surface.
5. The pen comes to rest on a flat plane.
   _(and 9 more)_

### Example 4

**Original**: twisting a cloth

**Paraphrases**:
1. Wringing out the fabric.
2. Turning the cloth to remove liquid.
3. Applying a twisting motion to the material.
4. Squeezing the cloth by twisting it.
5. The cloth is being contorted.
   _(and 10 more)_

### Example 5

**Original**: taking a slice of onion

**Paraphrases**:
1. The person is removing a single piece from the onion.
2. They are in the process of cutting off a portion of the onion.
3. A slice of the onion is being separated.
4. The individual is taking a thin piece of onion.
5. They are extracting a slice from the whole onion.
   _(and 9 more)_

### Example 6

**Original**: holding bulb

**Paraphrases**:
1. Grasping a lightbulb.
2. The hand is gripping the bulb.
3. A person's fingers are wrapped around a lightbulb.
4. The lightbulb is being held.
5. A hand is in contact with a bulb.
   _(and 9 more)_

### Example 7

**Original**: holding a pencil next to tissue box

**Paraphrases**:
1. A pencil is being held near a box of tissues.
2. The person's hand has a pencil, and it's positioned near a tissue box.
3. A pencil is placed beside a tissue box.
4. The scene shows a pencil and a tissue box, with the pencil being held close to the box.
5. A hand is holding a pencil, and a tissue box is nearby.
   _(and 9 more)_

### Example 8

**Original**: pretending to turn hat upside down

**Paraphrases**:
1. Mimicking the action of flipping a hat over.
2. Making a gesture as if inverting a hat.
3. Simulating the act of turning a hat inside out.
4. The person acts as though they are flipping their hat.
5. A playful movement suggesting the hat is being turned over.
   _(and 9 more)_

### Example 9

**Original**: folding paper towel

**Paraphrases**:
1. The person is in the process of creasing and layering a paper towel.
2. A paper towel is being manipulated to create folds.
3. The action involves repeatedly bending a paper towel.
4. Someone is making a paper towel smaller by folding it.
5. The paper towel is being folded over itself.
   _(and 10 more)_

### Example 10

**Original**: spreading margarine onto bread

**Paraphrases**:
1. Applying a layer of margarine to the surface of a slice of bread.
2. Using a knife to distribute margarine evenly across bread.
3. The act of buttering bread with margarine.
4. Coating bread with margarine using a utensil.
5. The process of putting margarine on a piece of bread.
   _(and 10 more)_

## Generation Method

Paraphrases were generated using an LLM (Google Gemini 2.0 Flash Lite) with the following prompt:

> "The following is an annotation of a video that accurately describes its spatial AND temporal content.
> Provide 4 to 20 paraphrased examples of this annotation. Ensure that the paraphrased examples maintain
> the same meaning as the original, as misalignment from the source video is detrimental."

## Usage

When training, randomly select either the original caption or one of the paraphrases for each video
to provide caption diversity during training while maintaining semantic consistency.

## Notes

- Paraphrases maintain the temporal and spatial aspects of the original captions
- Action descriptions are preserved to ensure video-caption alignment
- Some videos may have more paraphrases than others based on caption complexity
