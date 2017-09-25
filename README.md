# bootstrap-4-beta-validation
This css file extends the bootstrap 4-beta validation to work as bootstrap 3 did without having to be based on states changes.

This can be quite useful if you want to manage your own validation rather than letting bootstrap do it for you.

**Note: This does use fontawesome.io for the icons.**

JSFiddle Example: https://jsfiddle.net/lilpug/1m7heqqr/1/

## Normal Example (without validation)

```HTML
<div class="form-group">
    <label class="control-label col-sm-12" for="contactName">*Name:</label>
    <div class="col-sm-12">
        <div class="input-group">
            <div class="input-group-addon">
                <i class="fa fa-pencil-square-o"></i>
            </div>
            <input type="text" name="name" value="" class="form-control" required>
        </div>                           
    </div>
</div>
```

## Is Valid Example

*"is-valid"* - Is supplied at the "input-group" div level.

*"form-control-feedback is-valid"* - Is supplied on the icon outside of the "input-group" div.

```HTML
<div class="form-group">
    <label class="control-label col-sm-4" for="contactName">*Name:</label>
    <div class="col-sm-5">
        <div class="input-group is-valid">
            <div class="input-group-addon">
                <i class="fa fa-pencil-square-o"></i>
            </div>
            <input type="text" name="name" value="" class="form-control" required>
        </div>
        <i class="form-control-feedback is-valid fa fa-check"></i>                
    </div>
</div>
```

## Is Invalid Example

*"is-invalid"* - Is supplied at the "input-group" div level.

*"form-control-feedback is-invalid"* - Is supplied on the icon outside of the "input-group" div.

*"invalid-feedback"* - Is supplied after the icon which is outside of the "input-group" div.

```HTML
<div class="form-group">
    <label class="control-label col-sm-4" for="contactName">*Name:</label>
    <div class="col-sm-5">
        <div class="input-group is-invalid">
            <div class="input-group-addon">
                <i class="fa fa-pencil-square-o"></i>
            </div>
            <input type="text" name="name" value="" class="form-control" required>
        </div>
        <i class="form-control-feedback is-invalid fa fa-times"></i>
        <div class="invalid-feedback">
            <p>The name field is required.</p>
            <p>The input is not a valid email address.</p>
            <p>The message is required and cannot be empty</p>
        </div>
    </div>
</div>
```
