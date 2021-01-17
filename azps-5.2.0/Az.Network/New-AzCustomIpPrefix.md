---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
ms.openlocfilehash: 08df4120e762a7837376af7413504a8fce678230
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347429"
---
# <span data-ttu-id="46334-101">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="46334-101">New-AzCustomIpPrefix</span></span>

## <span data-ttu-id="46334-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46334-102">SYNOPSIS</span></span>
<span data-ttu-id="46334-103">CustomIpPrefix erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="46334-103">Creates a CustomIpPrefix resource</span></span>

## <span data-ttu-id="46334-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="46334-104">SYNTAX</span></span>

```
New-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> -Location <String> -Cidr <String>
 [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46334-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="46334-105">DESCRIPTION</span></span>
<span data-ttu-id="46334-106">A **New-AzCustomIpPrefix** parancsmag létrehoz egy CustomIpPrefix erőforrást.</span><span class="sxs-lookup"><span data-stu-id="46334-106">The **New-AzCustomIpPrefix** cmdlet creates a CustomIpPrefix resource.</span></span>

## <span data-ttu-id="46334-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="46334-107">EXAMPLES</span></span>

### <span data-ttu-id="46334-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="46334-108">Example 1</span></span>
```powershell
PS C:\> $myCustomIpPrefix = New-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Cidr 40.40.40.0/24 -Location westus
```

<span data-ttu-id="46334-109">Ez a parancs létrehoz egy új CustomIpPrefix erőforrást $prefixName névvel az erőforráscsoportban $rgName 40.40.40.0/24-es cidr értékekkel a WestUsban</span><span class="sxs-lookup"><span data-stu-id="46334-109">This command creates a new CustomIpPrefix resource with name $prefixName in resource group $rgName with a cidr of 40.40.40.0/24 in westus</span></span>

## <span data-ttu-id="46334-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46334-110">PARAMETERS</span></span>

### <span data-ttu-id="46334-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46334-111">-AsJob</span></span>
<span data-ttu-id="46334-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="46334-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46334-113">-Cidr</span><span class="sxs-lookup"><span data-stu-id="46334-113">-Cidr</span></span>
<span data-ttu-id="46334-114">A CustomIpPrefix CIDR.</span><span class="sxs-lookup"><span data-stu-id="46334-114">The CustomIpPrefix CIDR.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46334-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46334-115">-DefaultProfile</span></span>
<span data-ttu-id="46334-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="46334-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46334-117">-Location</span><span class="sxs-lookup"><span data-stu-id="46334-117">-Location</span></span>
<span data-ttu-id="46334-118">A CustomIpPrefix helye.</span><span class="sxs-lookup"><span data-stu-id="46334-118">The CustomIpPrefix location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46334-119">-Name</span><span class="sxs-lookup"><span data-stu-id="46334-119">-Name</span></span>
<span data-ttu-id="46334-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="46334-120">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46334-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46334-121">-ResourceGroupName</span></span>
<span data-ttu-id="46334-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="46334-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46334-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="46334-123">-Tag</span></span>
<span data-ttu-id="46334-124">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="46334-124">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46334-125">-Zone</span><span class="sxs-lookup"><span data-stu-id="46334-125">-Zone</span></span>
<span data-ttu-id="46334-126">A rendelkezésre állási zónák listája, amely az erőforráshoz kiosztott IP-címet sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="46334-126">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46334-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46334-127">-Confirm</span></span>
<span data-ttu-id="46334-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="46334-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46334-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46334-129">-WhatIf</span></span>
<span data-ttu-id="46334-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="46334-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46334-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="46334-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46334-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46334-132">CommonParameters</span></span>
<span data-ttu-id="46334-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46334-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46334-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46334-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46334-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46334-135">INPUTS</span></span>

### <span data-ttu-id="46334-136">System.String</span><span class="sxs-lookup"><span data-stu-id="46334-136">System.String</span></span>

### <span data-ttu-id="46334-137">System.String[]</span><span class="sxs-lookup"><span data-stu-id="46334-137">System.String[]</span></span>

### <span data-ttu-id="46334-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="46334-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="46334-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46334-139">OUTPUTS</span></span>

### <span data-ttu-id="46334-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="46334-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="46334-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="46334-141">NOTES</span></span>

## <span data-ttu-id="46334-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46334-142">RELATED LINKS</span></span>

[<span data-ttu-id="46334-143">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="46334-143">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="46334-144">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="46334-144">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="46334-145">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="46334-145">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)