---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
ms.openlocfilehash: 34c887388256e86657d1a979729333e44cb1bd77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494157"
---
# <span data-ttu-id="a9644-101">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a9644-101">New-AzureRmBatchApplication</span></span>

## <span data-ttu-id="a9644-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9644-102">SYNOPSIS</span></span>
<span data-ttu-id="a9644-103">Hozzáad egy alkalmazást a megadott köteg fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="a9644-103">Adds an application to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9644-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9644-104">SYNTAX</span></span>

```
New-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9644-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9644-105">DESCRIPTION</span></span>
<span data-ttu-id="a9644-106">A **New-AzureRmBatchApplication** parancsmag egy alkalmazást ad hozzá a megadott Azure-köteg fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="a9644-106">The **New-AzureRmBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="a9644-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a9644-107">EXAMPLES</span></span>

### <span data-ttu-id="a9644-108">Példa 1: üres alkalmazás hozzáadása egy köteg fiókhoz</span><span class="sxs-lookup"><span data-stu-id="a9644-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="a9644-109">Ez a parancs létrehozza a Bárdos Iparcikk alkalmazást az ContosoBatch-fiókban.</span><span class="sxs-lookup"><span data-stu-id="a9644-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="a9644-110">Az alkalmazás kezdetben nem tartalmaz csomagokat.</span><span class="sxs-lookup"><span data-stu-id="a9644-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="a9644-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9644-111">PARAMETERS</span></span>

### <span data-ttu-id="a9644-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a9644-112">-AccountName</span></span>
<span data-ttu-id="a9644-113">Annak a kötegelt fióknak a nevét adja meg, amelyre a parancsmag hozzáad egy alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="a9644-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="a9644-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="a9644-114">-AllowUpdates</span></span>
<span data-ttu-id="a9644-115">Itt adhatja meg, hogy az alkalmazásban lévő csomagokat felülírja-e ugyanazzal a verziójú karakterlánccal.</span><span class="sxs-lookup"><span data-stu-id="a9644-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9644-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a9644-116">-ApplicationId</span></span>
<span data-ttu-id="a9644-117">Az alkalmazás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9644-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="a9644-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9644-118">-DefaultProfile</span></span>
<span data-ttu-id="a9644-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9644-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9644-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a9644-120">-DisplayName</span></span>
<span data-ttu-id="a9644-121">Az alkalmazás megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9644-121">Specifies the display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9644-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9644-122">-ResourceGroupName</span></span>
<span data-ttu-id="a9644-123">A köteg fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9644-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="a9644-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9644-124">CommonParameters</span></span>
<span data-ttu-id="a9644-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9644-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9644-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9644-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9644-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9644-127">INPUTS</span></span>

### <span data-ttu-id="a9644-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a9644-128">System.String</span></span>

### <span data-ttu-id="a9644-129">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a9644-129">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a9644-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9644-130">OUTPUTS</span></span>

### <span data-ttu-id="a9644-131">Microsoft.Azure.Commands.BatCH. Modellek. PSApplication</span><span class="sxs-lookup"><span data-stu-id="a9644-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="a9644-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9644-132">NOTES</span></span>

## <span data-ttu-id="a9644-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9644-133">RELATED LINKS</span></span>

[<span data-ttu-id="a9644-134">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a9644-134">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="a9644-135">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a9644-135">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="a9644-136">Új – AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a9644-136">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="a9644-137">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a9644-137">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="a9644-138">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a9644-138">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="a9644-139">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a9644-139">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


