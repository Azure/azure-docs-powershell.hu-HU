---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 5c0af3ed67bd7cba3408b6628de70c7064120954
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017535"
---
# <span data-ttu-id="a0a51-101">New-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a0a51-101">New-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="a0a51-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0a51-102">SYNOPSIS</span></span>
<span data-ttu-id="a0a51-103">Új tárterületet hoz létre az eszköz Edge Storage (tároló) fiókjában.</span><span class="sxs-lookup"><span data-stu-id="a0a51-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="a0a51-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0a51-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0a51-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0a51-105">DESCRIPTION</span></span>
<span data-ttu-id="a0a51-106">A **New-AzStackEdgeStorageContainer** parancsmag új tárterületet hoz létre az Edge Storage (halom-tároló) eszközön.</span><span class="sxs-lookup"><span data-stu-id="a0a51-106">The **New-AzStackEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Stack Edge device.</span></span>

## <span data-ttu-id="a0a51-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a0a51-107">EXAMPLES</span></span>

### <span data-ttu-id="a0a51-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a0a51-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="a0a51-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0a51-109">PARAMETERS</span></span>

### <span data-ttu-id="a0a51-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0a51-110">-AsJob</span></span>
<span data-ttu-id="a0a51-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a0a51-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0a51-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="a0a51-112">-DataFormat</span></span>
<span data-ttu-id="a0a51-113">Az adatformátum beállítása: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="a0a51-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="a0a51-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0a51-114">-DefaultProfile</span></span>
<span data-ttu-id="a0a51-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0a51-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0a51-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a0a51-116">-DeviceName</span></span>
<span data-ttu-id="a0a51-117">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="a0a51-117">Device Name</span></span>

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

### <span data-ttu-id="a0a51-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a0a51-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="a0a51-119">Létező EdgeStorageAccount-név megadása</span><span class="sxs-lookup"><span data-stu-id="a0a51-119">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="a0a51-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a0a51-120">-Name</span></span>
<span data-ttu-id="a0a51-121">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="a0a51-121">Resource Name</span></span>

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

### <span data-ttu-id="a0a51-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0a51-122">-ResourceGroupName</span></span>
<span data-ttu-id="a0a51-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a0a51-123">Resource Group Name</span></span>

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

### <span data-ttu-id="a0a51-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a0a51-124">-Confirm</span></span>
<span data-ttu-id="a0a51-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a0a51-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0a51-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0a51-126">-WhatIf</span></span>
<span data-ttu-id="a0a51-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a0a51-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0a51-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a0a51-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0a51-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0a51-129">CommonParameters</span></span>
<span data-ttu-id="a0a51-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0a51-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0a51-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a0a51-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0a51-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0a51-132">INPUTS</span></span>

### <span data-ttu-id="a0a51-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a0a51-133">System.String</span></span>

## <span data-ttu-id="a0a51-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0a51-134">OUTPUTS</span></span>

### <span data-ttu-id="a0a51-135">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a0a51-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="a0a51-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0a51-136">NOTES</span></span>

## <span data-ttu-id="a0a51-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0a51-137">RELATED LINKS</span></span>
