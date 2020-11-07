---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 0ae0003c4c38b7e3922694ed01f6d8f4d10a49d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680434"
---
# <span data-ttu-id="bf495-101">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="bf495-101">Remove-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="bf495-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf495-102">SYNOPSIS</span></span>
<span data-ttu-id="bf495-103">Egy alkalmazáscsomag-rekord és a bináris fájl törlése</span><span class="sxs-lookup"><span data-stu-id="bf495-103">Deletes an application package record and the binary file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf495-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf495-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf495-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf495-105">DESCRIPTION</span></span>
<span data-ttu-id="bf495-106">A **Remove-AzureRmBatchApplicationPackage** parancsmag alkalmazásspecifikus csomagot és bináris fájlt töröl egy Azure-fiókból.</span><span class="sxs-lookup"><span data-stu-id="bf495-106">The **Remove-AzureRmBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="bf495-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bf495-107">EXAMPLES</span></span>

### <span data-ttu-id="bf495-108">1. példa: alkalmazáscsomag törlése egy köteg fiókból</span><span class="sxs-lookup"><span data-stu-id="bf495-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="bf495-109">Ez a parancs törli a Bárdos Iparcikk alkalmazás 1,0-ös verzióját a ContosoBatchGroup-fiókból.</span><span class="sxs-lookup"><span data-stu-id="bf495-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="bf495-110">A parancs törli mind a csomagot, mind a bináris fájlt tartalmazó blobot.</span><span class="sxs-lookup"><span data-stu-id="bf495-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="bf495-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf495-111">PARAMETERS</span></span>

### <span data-ttu-id="bf495-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bf495-112">-AccountName</span></span>
<span data-ttu-id="bf495-113">Annak a kötegelt fióknak a nevét adja meg, amelyből a parancsmag töröl egy alkalmazáscsomag.</span><span class="sxs-lookup"><span data-stu-id="bf495-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf495-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="bf495-114">-ApplicationId</span></span>
<span data-ttu-id="bf495-115">Az alkalmazás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf495-115">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf495-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="bf495-116">-ApplicationVersion</span></span>
<span data-ttu-id="bf495-117">Az alkalmazás verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf495-117">Specifies the version of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf495-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf495-118">-DefaultProfile</span></span>
<span data-ttu-id="bf495-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf495-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf495-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf495-120">-ResourceGroupName</span></span>
<span data-ttu-id="bf495-121">A köteg fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf495-121">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf495-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf495-122">CommonParameters</span></span>
<span data-ttu-id="bf495-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf495-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf495-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf495-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf495-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf495-125">INPUTS</span></span>

### <span data-ttu-id="bf495-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="bf495-126">None</span></span>
<span data-ttu-id="bf495-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="bf495-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bf495-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf495-128">OUTPUTS</span></span>

## <span data-ttu-id="bf495-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf495-129">NOTES</span></span>

## <span data-ttu-id="bf495-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf495-130">RELATED LINKS</span></span>

[<span data-ttu-id="bf495-131">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="bf495-131">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="bf495-132">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="bf495-132">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="bf495-133">Új – AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="bf495-133">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="bf495-134">Új – AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="bf495-134">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="bf495-135">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="bf495-135">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="bf495-136">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="bf495-136">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


