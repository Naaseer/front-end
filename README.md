# front-end
<div class="col-md-6" style="overflow-y: auto;"  (cdkDropListDropped)="drop($event)">
        <div class="drop" [style.border-width.px]="imagens.length > 0 ? 0: 3">
          <div class="abc">
              <ngb-carousel style="outline: none;" id="carousel" #carousel *ngIf="imagens" (slide)="change($event)">
                <ng-template *ngFor="let imgIdx of imagens; let i = index" [id]="i" ngbSlide>
                  <div class="picsum-img-wrapper">
                    <img [src]="imgIdx.Imagem" style="border-radius: 8px;" class="img-responsive Images">
                      </div>                    
                </ng-template>              
              </ngb-carousel>            
          </div>
        </div>
        <div class="row">
          <div class="Upcard" *ngFor="let imgIdx of imagens | slice:1" >
            <img class="img-responsive" [src]="imgIdx.Imagem" style="width: 100%; height: 100%">
          </div>
        </div>
      </div>
