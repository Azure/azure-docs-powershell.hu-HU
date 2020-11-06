---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: cd21c9ce84a96ada003eb6520c9a2a115df186cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503071"
---
# Set-AzureBatchPoolOSVersion

## Áttekintés
A megadott készlet operációs rendszerhez tartozó verziójának módosítása.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **set-AzureBatchPoolOSVersion** parancsmag a megadott készlet operációs rendszerének verziószámát módosítja.

## Példák

### 1. példa: a cél operációs rendszer verziójának beállítása
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

Ez a parancs a MyPool alkalmazáskészlet operációs rendszerének verziószámát a WA-GUEST-OS-4.20 _201505-01 értékre állítja.

## PARAMÉTEREK

### -BatchContext
Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.
Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni. Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével. A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos. A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Azonosító
A készlet AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -TargetOSVersion
Az Azure Guest Operating System verziószámát adja meg a készletben lévő virtuális gépeken való telepítéshez.
Az Azure vendég operációs rendszer verzióiról további információt az Azure Guest Operating OS kiadásai és az SDK kompatibilitási mátrixa (című témakörben találhat https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### BatchAccountContext
A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről

### Karakterlánc
Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)


