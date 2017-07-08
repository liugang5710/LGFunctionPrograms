# LGFunctionPrograms
一些特殊的功能需求

#### 动态UITableView 生成长截图 [http://www.jianshu.com/p/8756acb81cb5]
#code
____
+(UIImage *)getTableViewimagewithTabelview:(UITableView *)tableview{
    UIImage* viewImage = nil;
    UITableView *scrollView = tableview;
    UIGraphicsBeginImageContextWithOptions(scrollView.contentSize, scrollView.opaque, 0.0);
    {
        CGPoint savedContentOffset = scrollView.contentOffset;
        CGRect savedFrame = scrollView.frame;

        scrollView.contentOffset = CGPointZero;
        scrollView.frame = CGRectMake(0, 0, scrollView.contentSize.width, scrollView.contentSize.height);

        [scrollView.layer renderInContext: UIGraphicsGetCurrentContext()];
        viewImage = UIGraphicsGetImageFromCurrentImageContext();

        scrollView.contentOffset = savedContentOffset;
        scrollView.frame = savedFrame;
    }
    UIGraphicsEndImageContext();

    return viewImage;
}


# [http://www.hangge.com/blog/cache/category_72_1.html]
### 正在学习的博客 [https://juejin.im/post/5945187afe88c2006a74076a]
