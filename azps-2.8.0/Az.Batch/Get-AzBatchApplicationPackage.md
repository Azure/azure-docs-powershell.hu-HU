---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
ms.openlocfilehash: 0cbcc49f4b37b150b783467f45dcc7d4d7e53f2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667704"
---
# <span data-ttu-id="e284c-101">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e284c-101">Get-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="e284c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e284c-102">SYNOPSIS</span></span>
<span data-ttu-id="e284c-103">A kötegelt fiókokban lévő alkalmazáscsomag adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e284c-103">Gets information about an application package in a Batch account.</span></span>

## <span data-ttu-id="e284c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e284c-104">SYNTAX</span></span>

```
Get-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e284c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e284c-105">DESCRIPTION</span></span>
<span data-ttu-id="e284c-106">A **Get-AzBatchApplicationPackage** parancsmag egy Azure-köteg-fiókban lévő alkalmazáscsomag adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e284c-106">The **Get-AzBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="e284c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e284c-107">EXAMPLES</span></span>

### <span data-ttu-id="e284c-108">1. példa: egy alkalmazáscsomag részleteinek beszerzése egy köteg fiókban</span><span class="sxs-lookup"><span data-stu-id="e284c-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="e284c-109">Ez a parancs a Bárdos Iparcikk-csomag 1,0-as verziójának részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e284c-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="e284c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e284c-110">PARAMETERS</span></span>

### <span data-ttu-id="e284c-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e284c-111">-AccountName</span></span>
<span data-ttu-id="e284c-112">Annak a kötegelt fióknak a neve, amelyből a parancsmag információt kap.</span><span class="sxs-lookup"><span data-stu-id="e284c-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="e284c-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e284c-113">-ApplicationId</span></span>
<span data-ttu-id="e284c-114">Az alkalmazás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e284c-114">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e284c-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="e284c-115">-ApplicationVersion</span></span>
<span data-ttu-id="e284c-116">Az alkalmazás verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e284c-116">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="e284c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e284c-117">-DefaultProfile</span></span>
<span data-ttu-id="e284c-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e284c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e284c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e284c-119">-ResourceGroupName</span></span>
<span data-ttu-id="e284c-120">A köteg fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e284c-120">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="e284c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e284c-121">CommonParameters</span></span>
<span data-ttu-id="e284c-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e284c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e284c-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e284c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e284c-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e284c-124">INPUTS</span></span>

### <span data-ttu-id="e284c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e284c-125">System.String</span></span>

## <span data-ttu-id="e284c-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e284c-126">OUTPUTS</span></span>

### <span data-ttu-id="e284c-127">Microsoft.Azure.Commands.BatCH. Modellek. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e284c-127">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="e284c-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e284c-128">NOTES</span></span>

## <span data-ttu-id="e284c-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e284c-129">RELATED LINKS</span></span>

[<span data-ttu-id="e284c-130">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e284c-130">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="e284c-131">Új – AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e284c-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="e284c-132">Új – AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e284c-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="e284c-133">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e284c-133">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="e284c-134">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e284c-134">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="e284c-135">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e284c-135">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


