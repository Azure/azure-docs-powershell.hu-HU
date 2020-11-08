---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 0d3f3a34257ad32c8b606b99c3f7170fb15684b0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195632"
---
# <span data-ttu-id="3d23f-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="3d23f-101">Remove-AzHost</span></span>

## <span data-ttu-id="3d23f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d23f-102">SYNOPSIS</span></span>
<span data-ttu-id="3d23f-103">Egy állomás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="3d23f-103">Removes a host.</span></span>

## <span data-ttu-id="3d23f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d23f-104">SYNTAX</span></span>

### <span data-ttu-id="3d23f-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3d23f-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d23f-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="3d23f-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d23f-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="3d23f-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d23f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d23f-108">DESCRIPTION</span></span>
<span data-ttu-id="3d23f-109">Ez a parancsmag egy állomás törlését fogja törölni.</span><span class="sxs-lookup"><span data-stu-id="3d23f-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="3d23f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3d23f-110">EXAMPLES</span></span>

### <span data-ttu-id="3d23f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3d23f-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="3d23f-112">Ez a parancs a megadott állomást kapja és távolítja el.</span><span class="sxs-lookup"><span data-stu-id="3d23f-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="3d23f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="3d23f-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="3d23f-114">Ez a parancs eltávolítja a megadott állomást.</span><span class="sxs-lookup"><span data-stu-id="3d23f-114">This command removes the given host.</span></span>

## <span data-ttu-id="3d23f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d23f-115">PARAMETERS</span></span>

### <span data-ttu-id="3d23f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d23f-116">-AsJob</span></span>
<span data-ttu-id="3d23f-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3d23f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d23f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d23f-118">-DefaultProfile</span></span>
<span data-ttu-id="3d23f-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3d23f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d23f-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="3d23f-120">-HostGroupName</span></span>
<span data-ttu-id="3d23f-121">A Host csoport neve.</span><span class="sxs-lookup"><span data-stu-id="3d23f-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d23f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d23f-122">-InputObject</span></span>
<span data-ttu-id="3d23f-123">Az állomás helyi objektuma.</span><span class="sxs-lookup"><span data-stu-id="3d23f-123">The local object of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHost
Parameter Sets: ObjectParameter
Aliases: Host

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d23f-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3d23f-124">-Name</span></span>
<span data-ttu-id="3d23f-125">Az állomás neve.</span><span class="sxs-lookup"><span data-stu-id="3d23f-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d23f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d23f-126">-ResourceGroupName</span></span>
<span data-ttu-id="3d23f-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3d23f-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d23f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d23f-128">-ResourceId</span></span>
<span data-ttu-id="3d23f-129">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3d23f-129">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d23f-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3d23f-130">-Confirm</span></span>
<span data-ttu-id="3d23f-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3d23f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d23f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d23f-132">-WhatIf</span></span>
<span data-ttu-id="3d23f-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3d23f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d23f-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3d23f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d23f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d23f-135">CommonParameters</span></span>
<span data-ttu-id="3d23f-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d23f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d23f-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3d23f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d23f-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d23f-138">INPUTS</span></span>

### <span data-ttu-id="3d23f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3d23f-139">System.String</span></span>

### <span data-ttu-id="3d23f-140">Microsoft. Azure. commands. számítási. Automation. models. PSHost</span><span class="sxs-lookup"><span data-stu-id="3d23f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="3d23f-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d23f-141">OUTPUTS</span></span>

### <span data-ttu-id="3d23f-142">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="3d23f-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3d23f-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d23f-143">NOTES</span></span>

## <span data-ttu-id="3d23f-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d23f-144">RELATED LINKS</span></span>
