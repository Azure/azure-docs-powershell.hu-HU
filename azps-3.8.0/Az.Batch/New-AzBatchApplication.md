---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
ms.openlocfilehash: 44d3c44effa74844713f6ecdf3012109f29b61b6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012446"
---
# <span data-ttu-id="67e91-101">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="67e91-101">New-AzBatchApplication</span></span>

## <span data-ttu-id="67e91-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67e91-102">SYNOPSIS</span></span>
<span data-ttu-id="67e91-103">Hozzáad egy alkalmazást a megadott köteg fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="67e91-103">Adds an application to the specified Batch account.</span></span>

## <span data-ttu-id="67e91-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67e91-104">SYNTAX</span></span>

```
New-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67e91-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="67e91-105">DESCRIPTION</span></span>
<span data-ttu-id="67e91-106">A **New-AzBatchApplication** parancsmag egy alkalmazást ad hozzá a megadott Azure-köteg fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="67e91-106">The **New-AzBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="67e91-107">Példák</span><span class="sxs-lookup"><span data-stu-id="67e91-107">EXAMPLES</span></span>

### <span data-ttu-id="67e91-108">Példa 1: üres alkalmazás hozzáadása egy köteg fiókhoz</span><span class="sxs-lookup"><span data-stu-id="67e91-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="67e91-109">Ez a parancs létrehozza a Bárdos Iparcikk alkalmazást az ContosoBatch-fiókban.</span><span class="sxs-lookup"><span data-stu-id="67e91-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="67e91-110">Az alkalmazás kezdetben nem tartalmaz csomagokat.</span><span class="sxs-lookup"><span data-stu-id="67e91-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="67e91-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67e91-111">PARAMETERS</span></span>

### <span data-ttu-id="67e91-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="67e91-112">-AccountName</span></span>
<span data-ttu-id="67e91-113">Annak a kötegelt fióknak a nevét adja meg, amelyre a parancsmag hozzáad egy alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="67e91-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="67e91-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="67e91-114">-AllowUpdates</span></span>
<span data-ttu-id="67e91-115">Itt adhatja meg, hogy az alkalmazásban lévő csomagokat felülírja-e ugyanazzal a verziójú karakterlánccal.</span><span class="sxs-lookup"><span data-stu-id="67e91-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

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

### <span data-ttu-id="67e91-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="67e91-116">-ApplicationName</span></span>
<span data-ttu-id="67e91-117">Az alkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="67e91-117">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="67e91-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e91-118">-DefaultProfile</span></span>
<span data-ttu-id="67e91-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="67e91-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67e91-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="67e91-120">-DisplayName</span></span>
<span data-ttu-id="67e91-121">Az alkalmazás megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="67e91-121">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="67e91-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67e91-122">-ResourceGroupName</span></span>
<span data-ttu-id="67e91-123">A köteg fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="67e91-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="67e91-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e91-124">CommonParameters</span></span>
<span data-ttu-id="67e91-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67e91-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67e91-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="67e91-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e91-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67e91-127">INPUTS</span></span>

### <span data-ttu-id="67e91-128">System. String</span><span class="sxs-lookup"><span data-stu-id="67e91-128">System.String</span></span>

### <span data-ttu-id="67e91-129">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="67e91-129">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="67e91-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67e91-130">OUTPUTS</span></span>

### <span data-ttu-id="67e91-131">Microsoft.Azure.Commands.BatCH. Modellek. PSApplication</span><span class="sxs-lookup"><span data-stu-id="67e91-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="67e91-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67e91-132">NOTES</span></span>

## <span data-ttu-id="67e91-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67e91-133">RELATED LINKS</span></span>

[<span data-ttu-id="67e91-134">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="67e91-134">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="67e91-135">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="67e91-135">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="67e91-136">Új – AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="67e91-136">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="67e91-137">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="67e91-137">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="67e91-138">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="67e91-138">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="67e91-139">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="67e91-139">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


