---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: f260af1bc26d9cf921a26e4f08c3c4feab4b79c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497131"
---
# <span data-ttu-id="0934a-101">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="0934a-101">Get-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="0934a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0934a-102">SYNOPSIS</span></span>
<span data-ttu-id="0934a-103">A kötegelt fiókokban lévő alkalmazáscsomag adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0934a-103">Gets information about an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0934a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0934a-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0934a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0934a-105">DESCRIPTION</span></span>
<span data-ttu-id="0934a-106">A **Get-AzureRmBatchApplicationPackage** parancsmag egy Azure-köteg-fiókban lévő alkalmazáscsomag adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0934a-106">The **Get-AzureRmBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="0934a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0934a-107">EXAMPLES</span></span>

### <span data-ttu-id="0934a-108">1. példa: egy alkalmazáscsomag részleteinek beszerzése egy köteg fiókban</span><span class="sxs-lookup"><span data-stu-id="0934a-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="0934a-109">Ez a parancs a Bárdos Iparcikk-csomag 1,0-as verziójának részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0934a-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="0934a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0934a-110">PARAMETERS</span></span>

### <span data-ttu-id="0934a-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0934a-111">-AccountName</span></span>
<span data-ttu-id="0934a-112">Annak a kötegelt fióknak a neve, amelyből a parancsmag információt kap.</span><span class="sxs-lookup"><span data-stu-id="0934a-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="0934a-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0934a-113">-ApplicationId</span></span>
<span data-ttu-id="0934a-114">Az alkalmazás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0934a-114">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="0934a-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="0934a-115">-ApplicationVersion</span></span>
<span data-ttu-id="0934a-116">Az alkalmazás verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0934a-116">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="0934a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0934a-117">-ResourceGroupName</span></span>
<span data-ttu-id="0934a-118">A köteg fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0934a-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="0934a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0934a-119">-DefaultProfile</span></span>
<span data-ttu-id="0934a-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0934a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0934a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0934a-121">CommonParameters</span></span>
<span data-ttu-id="0934a-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0934a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0934a-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0934a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0934a-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0934a-124">INPUTS</span></span>

## <span data-ttu-id="0934a-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0934a-125">OUTPUTS</span></span>

### <span data-ttu-id="0934a-126">Microsoft.Azure.Commands.BatCH. Modellek. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="0934a-126">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="0934a-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0934a-127">NOTES</span></span>

## <span data-ttu-id="0934a-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0934a-128">RELATED LINKS</span></span>

[<span data-ttu-id="0934a-129">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="0934a-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="0934a-130">Új – AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="0934a-130">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="0934a-131">Új – AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="0934a-131">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="0934a-132">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="0934a-132">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="0934a-133">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="0934a-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="0934a-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="0934a-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


