---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 3561c77e79f0ee1be82b8f180fdf1b73879dc084
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163834"
---
# <span data-ttu-id="594e5-101">New-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="594e5-101">New-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="594e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="594e5-102">SYNOPSIS</span></span>
<span data-ttu-id="594e5-103">Létrehoz egy új tárolót az eszköz Edge Storage-fiókjában.</span><span class="sxs-lookup"><span data-stu-id="594e5-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="594e5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="594e5-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="594e5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="594e5-105">DESCRIPTION</span></span>
<span data-ttu-id="594e5-106">A **New-AzDataBoxEdgeStorageContainer** parancsmag új tárolót hoz létre a Edge Storage-fiókban egy Data Box Edge-eszközön.</span><span class="sxs-lookup"><span data-stu-id="594e5-106">The **New-AzDataBoxEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Data Box Edge device.</span></span>

## <span data-ttu-id="594e5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="594e5-107">EXAMPLES</span></span>

### <span data-ttu-id="594e5-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="594e5-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="594e5-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="594e5-109">PARAMETERS</span></span>

### <span data-ttu-id="594e5-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="594e5-110">-AsJob</span></span>
<span data-ttu-id="594e5-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="594e5-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="594e5-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="594e5-112">-DataFormat</span></span>
<span data-ttu-id="594e5-113">Adatformátum beállítása például: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="594e5-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="594e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="594e5-114">-DefaultProfile</span></span>
<span data-ttu-id="594e5-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="594e5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="594e5-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="594e5-116">-DeviceName</span></span>
<span data-ttu-id="594e5-117">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="594e5-117">Device Name</span></span>

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

### <span data-ttu-id="594e5-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="594e5-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="594e5-119">Meglévő EdgeStorageAccount nevének meg kell adnia</span><span class="sxs-lookup"><span data-stu-id="594e5-119">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="594e5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="594e5-120">-Name</span></span>
<span data-ttu-id="594e5-121">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="594e5-121">Resource Name</span></span>

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

### <span data-ttu-id="594e5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="594e5-122">-ResourceGroupName</span></span>
<span data-ttu-id="594e5-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="594e5-123">Resource Group Name</span></span>

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

### <span data-ttu-id="594e5-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="594e5-124">-Confirm</span></span>
<span data-ttu-id="594e5-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="594e5-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="594e5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="594e5-126">-WhatIf</span></span>
<span data-ttu-id="594e5-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="594e5-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="594e5-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="594e5-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="594e5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="594e5-129">CommonParameters</span></span>
<span data-ttu-id="594e5-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="594e5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="594e5-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="594e5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="594e5-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="594e5-132">INPUTS</span></span>

### <span data-ttu-id="594e5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="594e5-133">System.String</span></span>

## <span data-ttu-id="594e5-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="594e5-134">OUTPUTS</span></span>

### <span data-ttu-id="594e5-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="594e5-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="594e5-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="594e5-136">NOTES</span></span>

## <span data-ttu-id="594e5-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="594e5-137">RELATED LINKS</span></span>
