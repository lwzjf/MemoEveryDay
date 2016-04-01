# MemoEveryDay

#iOS9 Shortcut Bar only mode 

CGRect keyboardScreenEndFrame = [[info objectForKey:UIKeyboardFrameEndUserInfoKey] CGRectValue];
CGRect keyboardViewEndFrame = [self.view convertRect:keyboardScreenEndFrame fromView:self.view.window];
CGRect keyboardFrame = CGRectIntersection(self.view.bounds, keyboardViewEndFrame); //!imporant
CGFloat keyboardHeight = keyboardFrame.size.height; // = 55


reference :
http://stackoverflow.com/questions/32319697/view-aligned-to-top-of-keyboard-appears-in-wrong-place-in-ios-9-shortcut-bar-onl
