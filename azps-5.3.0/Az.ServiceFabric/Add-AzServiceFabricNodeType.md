---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
ms.openlocfilehash: de512f636b0a326029981e199b13926a9fc5824a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479579"
---
# <span data-ttu-id="784a8-101">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="784a8-101">Add-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="784a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="784a8-102">SYNOPSIS</span></span>
<span data-ttu-id="784a8-103">Új csomóponttípus hozzáadása a meglévő fürthöz.</span><span class="sxs-lookup"><span data-stu-id="784a8-103">Add a new node type to the existing cluster.</span></span>

## <span data-ttu-id="784a8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="784a8-104">SYNTAX</span></span>

```
Add-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="784a8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="784a8-105">DESCRIPTION</span></span>
<span data-ttu-id="784a8-106">Vegyen fel egy új csomóponttípust egy meglévő fürtbe.</span><span class="sxs-lookup"><span data-stu-id="784a8-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="784a8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="784a8-107">EXAMPLES</span></span>

### <span data-ttu-id="784a8-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="784a8-108">Example 1</span></span>
```powershell
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="784a8-109">Ez a parancs hozzáad egy új NodeType 'n2'-t 5-ös kapacitással, a vm-rendszergazda neve pedig "adminName".</span><span class="sxs-lookup"><span data-stu-id="784a8-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="784a8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="784a8-110">PARAMETERS</span></span>

### <span data-ttu-id="784a8-111">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="784a8-111">-Capacity</span></span>
<span data-ttu-id="784a8-112">Kapacitás</span><span class="sxs-lookup"><span data-stu-id="784a8-112">Capacity</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="784a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="784a8-113">-DefaultProfile</span></span>
<span data-ttu-id="784a8-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="784a8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="784a8-115">–10.</span><span class="sxs-lookup"><span data-stu-id="784a8-115">-DurabilityLevel</span></span>
<span data-ttu-id="784a8-116">Adja meg a NodeType minőségének szintjét.</span><span class="sxs-lookup"><span data-stu-id="784a8-116">Specify the durability level of the NodeType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases:
Accepted values: Bronze, Silver, Gold

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="784a8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="784a8-117">-Name</span></span>
<span data-ttu-id="784a8-118">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="784a8-118">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="784a8-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="784a8-119">-NodeType</span></span>
<span data-ttu-id="784a8-120">A csomóponttípus neve</span><span class="sxs-lookup"><span data-stu-id="784a8-120">The node type name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="784a8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="784a8-121">-ResourceGroupName</span></span>
<span data-ttu-id="784a8-122">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="784a8-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="784a8-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="784a8-123">-Tier</span></span>
<span data-ttu-id="784a8-124">Vm Sku Tier</span><span class="sxs-lookup"><span data-stu-id="784a8-124">Vm Sku Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="784a8-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="784a8-125">-VmPassword</span></span>
<span data-ttu-id="784a8-126">A Vm gépre való bejelentkezéshez használt jelszó</span><span class="sxs-lookup"><span data-stu-id="784a8-126">The password for login to the Vm</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="784a8-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="784a8-127">-VmSku</span></span>
<span data-ttu-id="784a8-128">A termékváltozat neve</span><span class="sxs-lookup"><span data-stu-id="784a8-128">The sku name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="784a8-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="784a8-129">-VmUserName</span></span>
<span data-ttu-id="784a8-130">A Vm szolgáltatásba való naplózáshoz megadott felhasználónév</span><span class="sxs-lookup"><span data-stu-id="784a8-130">The user name for logging to Vm</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="784a8-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="784a8-131">-Confirm</span></span>
<span data-ttu-id="784a8-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="784a8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="784a8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="784a8-133">-WhatIf</span></span>
<span data-ttu-id="784a8-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="784a8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="784a8-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="784a8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="784a8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="784a8-136">CommonParameters</span></span>
<span data-ttu-id="784a8-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="784a8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="784a8-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="784a8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="784a8-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="784a8-139">INPUTS</span></span>

### <span data-ttu-id="784a8-140">System.String</span><span class="sxs-lookup"><span data-stu-id="784a8-140">System.String</span></span>

### <span data-ttu-id="784a8-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="784a8-141">System.Int32</span></span>

### <span data-ttu-id="784a8-142">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="784a8-142">System.Security.SecureString</span></span>

### <span data-ttu-id="784a8-143">Microsoft.Azure.Commands.ServiceFabric.Models.Fogaraslevel</span><span class="sxs-lookup"><span data-stu-id="784a8-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="784a8-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="784a8-144">OUTPUTS</span></span>

### <span data-ttu-id="784a8-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="784a8-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="784a8-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="784a8-146">NOTES</span></span>

## <span data-ttu-id="784a8-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="784a8-147">RELATED LINKS</span></span>
