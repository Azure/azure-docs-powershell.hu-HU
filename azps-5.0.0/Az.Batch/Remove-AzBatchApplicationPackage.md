---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: f88994649281d442f37a2bafa2cf2b4f74e6b86e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187073"
---
# <span data-ttu-id="51de2-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="51de2-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="51de2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51de2-102">SYNOPSIS</span></span>
<span data-ttu-id="51de2-103">Egy alkalmazáscsomag-rekord és a bináris fájl törlése</span><span class="sxs-lookup"><span data-stu-id="51de2-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="51de2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51de2-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationName] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="51de2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="51de2-105">DESCRIPTION</span></span>
<span data-ttu-id="51de2-106">A **Remove-AzBatchApplicationPackage** parancsmag alkalmazásspecifikus csomagot és bináris fájlt töröl egy Azure-fiókból.</span><span class="sxs-lookup"><span data-stu-id="51de2-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="51de2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="51de2-107">EXAMPLES</span></span>

### <span data-ttu-id="51de2-108">1. példa: alkalmazáscsomag törlése egy köteg fiókból</span><span class="sxs-lookup"><span data-stu-id="51de2-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="51de2-109">Ez a parancs törli a Bárdos Iparcikk alkalmazás 1,0-ös verzióját a ContosoBatchGroup-fiókból.</span><span class="sxs-lookup"><span data-stu-id="51de2-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="51de2-110">A parancs törli mind a csomagot, mind a bináris fájlt tartalmazó blobot.</span><span class="sxs-lookup"><span data-stu-id="51de2-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="51de2-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51de2-111">PARAMETERS</span></span>

### <span data-ttu-id="51de2-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="51de2-112">-AccountName</span></span>
<span data-ttu-id="51de2-113">Annak a kötegelt fióknak a nevét adja meg, amelyből a parancsmag töröl egy alkalmazáscsomag.</span><span class="sxs-lookup"><span data-stu-id="51de2-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51de2-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="51de2-114">-ApplicationName</span></span>
<span data-ttu-id="51de2-115">Az alkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="51de2-115">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51de2-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="51de2-116">-ApplicationVersion</span></span>
<span data-ttu-id="51de2-117">Az alkalmazás verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="51de2-117">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51de2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51de2-118">-DefaultProfile</span></span>
<span data-ttu-id="51de2-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51de2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51de2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51de2-120">-ResourceGroupName</span></span>
<span data-ttu-id="51de2-121">A köteg fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="51de2-121">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51de2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51de2-122">CommonParameters</span></span>
<span data-ttu-id="51de2-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51de2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51de2-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="51de2-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51de2-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51de2-125">INPUTS</span></span>

### <span data-ttu-id="51de2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="51de2-126">System.String</span></span>

## <span data-ttu-id="51de2-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51de2-127">OUTPUTS</span></span>

### <span data-ttu-id="51de2-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="51de2-128">System.Void</span></span>

## <span data-ttu-id="51de2-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51de2-129">NOTES</span></span>

## <span data-ttu-id="51de2-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51de2-130">RELATED LINKS</span></span>

[<span data-ttu-id="51de2-131">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="51de2-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="51de2-132">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="51de2-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="51de2-133">Új – AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="51de2-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="51de2-134">Új – AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="51de2-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="51de2-135">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="51de2-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="51de2-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="51de2-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


