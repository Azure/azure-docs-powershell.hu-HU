---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 5c0af3ed67bd7cba3408b6628de70c7064120954
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155090"
---
# <span data-ttu-id="f7501-101">New-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f7501-101">New-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="f7501-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7501-102">SYNOPSIS</span></span>
<span data-ttu-id="f7501-103">Létrehoz egy új tárolót az eszköz Edge Storage-fiókjában.</span><span class="sxs-lookup"><span data-stu-id="f7501-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="f7501-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f7501-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7501-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f7501-105">DESCRIPTION</span></span>
<span data-ttu-id="f7501-106">A **New-AzStackEdgeStorageContainer** parancsmag létrehoz egy új tárolót a Stack Edge-eszközön a Edge Storage-fiókban.</span><span class="sxs-lookup"><span data-stu-id="f7501-106">The **New-AzStackEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Stack Edge device.</span></span>

## <span data-ttu-id="f7501-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f7501-107">EXAMPLES</span></span>

### <span data-ttu-id="f7501-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f7501-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="f7501-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7501-109">PARAMETERS</span></span>

### <span data-ttu-id="f7501-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7501-110">-AsJob</span></span>
<span data-ttu-id="f7501-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f7501-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7501-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="f7501-112">-DataFormat</span></span>
<span data-ttu-id="f7501-113">Adatformátum beállítása például: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="f7501-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="f7501-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7501-114">-DefaultProfile</span></span>
<span data-ttu-id="f7501-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7501-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7501-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f7501-116">-DeviceName</span></span>
<span data-ttu-id="f7501-117">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="f7501-117">Device Name</span></span>

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

### <span data-ttu-id="f7501-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f7501-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="f7501-119">Meglévő EdgeStorageAccount nevének meg kell adnia</span><span class="sxs-lookup"><span data-stu-id="f7501-119">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="f7501-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f7501-120">-Name</span></span>
<span data-ttu-id="f7501-121">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="f7501-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7501-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7501-122">-ResourceGroupName</span></span>
<span data-ttu-id="f7501-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f7501-123">Resource Group Name</span></span>

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

### <span data-ttu-id="f7501-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7501-124">-Confirm</span></span>
<span data-ttu-id="f7501-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f7501-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7501-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7501-126">-WhatIf</span></span>
<span data-ttu-id="f7501-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f7501-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7501-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f7501-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7501-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7501-129">CommonParameters</span></span>
<span data-ttu-id="f7501-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7501-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7501-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7501-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7501-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7501-132">INPUTS</span></span>

### <span data-ttu-id="f7501-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f7501-133">System.String</span></span>

## <span data-ttu-id="f7501-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7501-134">OUTPUTS</span></span>

### <span data-ttu-id="f7501-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f7501-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="f7501-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f7501-136">NOTES</span></span>

## <span data-ttu-id="f7501-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7501-137">RELATED LINKS</span></span>
