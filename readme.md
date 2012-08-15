# ProcessWire Image Effects


## Description


A module that makes it easy to add effects to images in ProcessWire <http://www.processwire.com>
Note that this module may increase your amount of images dramatically.

## Installation


Drage the "imageeffects" folder to your modules directory.

## Usage Examples

See also the examples/home.php template example

		$image = $img->size($intWidth, $intHeight);
		echo "<img id='photo' src='{$image->url}' alt='{$image->description}' width='{$image->width}' height='{$image->height}' />" . $nl;

		$image = $img->size($intWidth, $intHeight)->fx(FieldtypeImageEffects::FX_DREAMY);
		echo "<img id='photo' src='{$image->url}' alt='{$image->description}' width='{$image->width}' height='{$image->height}' />" . $nl;

		$image = $img->size($intWidth, $intHeight)->fx(FieldtypeImageEffects::FX_GOTHAM, 5, 1);
		echo "<img id='photo' src='{$image->url}' alt='{$image->description}' width='{$image->width}' height='{$image->height}' />" . $nl;

		$image = $img->size($intWidth, $intHeight)->fx(FieldtypeImageEffects::FX_NASHVILLE);
		echo "<img id='photo' src='{$image->url}' alt='{$image->description}' width='{$image->width}' height='{$image->height}' />" . $nl;


		$image = $img->size($intWidth, $intHeight)->fx(FieldtypeImageEffects::FX_TOASTER, 2.2);
		echo "<img id='photo' src='{$image->url}' alt='{$image->description}' width='{$image->width}' height='{$image->height}' />" . $nl;

		$image = $img->size($intWidth, $intHeight)->fx(FieldtypeImageEffects::FX_KELVIN);
		echo "<img id='photo' src='{$image->url}' alt='{$image->description}' width='{$image->width}' height='{$image->height}' />" . $nl;


		$image = $img
			->size($intWidth, $intHeight)
			->fx(FieldtypeImageEffects::FX_TOASTER, 2.2)
			->fx(FieldtypeImageEffects::FX_ADD, FieldtypeImageEffects::IMG_SCRATCHES_03, 100, FieldtypeImageEffects::BLEND_COLOR_DODGE);
		echo "<img id='photo' src='{$image->url}' alt='{$image->description}' width='{$image->width}' height='{$image->height}' />" . $nl;


		$image = $img->size($intWidth, $intHeight)->fx(FieldtypeImageEffects::FX_ADD, FieldtypeImageEffects::IMG_SCRATCHES_02, 10, FieldtypeImageEffects::BLEND_COLOR_BURN );
		echo "<img id='photo' src='{$image->url}' alt='{$image->description}' width='{$image->width}' height='{$image->height}' />" . $nl;

		$image = $img
			->size($intWidth, $intHeight)
			->fx(FieldtypeImageEffects::FX_TOASTER, 2.2)
			->fx(FieldtypeImageEffects::FX_ADD, FieldtypeImageEffects::IMG_SCRATCHES_01, 100, FieldtypeImageEffects::BLEND_LINEAR_DODGE)
			->fx(FieldtypeImageEffects::FX_ADD, FieldtypeImageEffects::IMG_POLAROID_01, 100, FieldtypeImageEffects::BLEND_NORMAL);
		echo "<img id='photo' src='{$image->url}' alt='{$image->description}' width='{$image->width}' height='{$image->height}' />" . $nl;

		$image = $img
			->size($intWidth, $intHeight)
			->fx(FieldtypeImageEffects::FX_TOASTER, 2.2)
			->fx(FieldtypeImageEffects::FX_ADD, FieldtypeImageEffects::IMG_POLAROID_01, 100, FieldtypeImageEffects::BLEND_NORMAL)
			->fx(FieldtypeImageEffects::FX_ADD, FieldtypeImageEffects::IMG_SCRATCHES_02, 10, FieldtypeImageEffects::BLEND_HARD_LIGHT);
		echo "<img id='photo' src='{$image->url}' alt='{$image->description}' width='{$image->width}' height='{$image->height}' />" . $nl;


		$image = $img
			->size($intWidth, $intHeight)
			->fx(FieldtypeImageEffects::FX_WATERMARK, FieldtypeImageEffects::IMG_WATERMARK_01);
		echo "<img id='photo' src='{$image->url}' alt='{$image->description}' width='{$image->width}' height='{$image->height}' />" . $nl;

		$image = $img
			->size($intWidth, $intHeight)
			->fx(FieldtypeImageEffects::FX_SEPIA, 65);
		echo "<img id='photo' src='{$image->url}' alt='{$image->description}' width='{$image->width}' height='{$image->height}' />" . $nl;

		$image = $img
			->size($intWidth, $intHeight)
			->fx(FieldtypeImageEffects::FX_FOCAL_BLUR, 10);
		echo "<img id='photo' src='{$image->url}' alt='{$image->description}' width='{$image->width}' height='{$image->height}' />" . $nl;

		$image = $img
			->size($intWidth, $intHeight)
			->fx(FieldtypeImageEffects::FX_BLUR, 10);
		echo "<img id='photo' src='{$image->url}' alt='{$image->description}' width='{$image->width}' height='{$image->height}' />" . $nl;

		$image = $img->size($intWidth, $intHeight)
			->fx(FieldtypeImageEffects::FX_TOASTER, 2.2)
			->fx(FieldtypeImageEffects::FX_ADD, FieldtypeImageEffects::IMG_SCRATCHES_01, 50, FieldtypeImageEffects::BLEND_OVERLAY)
			->fx(FieldtypeImageEffects::FX_ADD, FieldtypeImageEffects::IMG_POLAROID_01, 100, FieldtypeImageEffects::BLEND_NORMAL);
		echo "<img id='photo' src='{$image->url}' alt='{$image->description}' width='{$image->width}' height='{$image->height}' />" . $nl;

		$image = $img->size($intWidth, $intHeight)
			->fx(FieldtypeImageEffects::FX_FOCAL_BLUR, 30)
			->fx(FieldtypeImageEffects::FX_TOASTER, 1.2)
			->fx(FieldtypeImageEffects::FX_ADD, FieldtypeImageEffects::IMG_SCRATCHES_01, 50, FieldtypeImageEffects::BLEND_COLOR_DODGE)
			->fx(FieldtypeImageEffects::FX_ADD, FieldtypeImageEffects::IMG_POLAROID_01, 100, FieldtypeImageEffects::BLEND_NORMAL);
		echo "<img id='photo' src='{$image->url}' alt='{$image->description}' width='{$image->width}' height='{$image->height}' />" . $nl;


## Output Examples

![Example output](https://raw.github.com/sommerper/ProcessWireImageEffects/ProcessWireImageEffects/examples/Basic%20Example%20Site.png)
