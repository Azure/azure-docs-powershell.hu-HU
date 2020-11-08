---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
ms.openlocfilehash: de512f636b0a326029981e199b13926a9fc5824a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181379"
---
# <span data-ttu-id="88f14-101">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="88f14-101">Add-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="88f14-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88f14-102">SYNOPSIS</span></span>
<span data-ttu-id="88f14-103">Új csomópont-típus felvétele a meglévő fürtbe.</span><span class="sxs-lookup"><span data-stu-id="88f14-103">Add a new node type to the existing cluster.</span></span>

## <span data-ttu-id="88f14-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88f14-104">SYNTAX</span></span>

```
Add-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88f14-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="88f14-105">DESCRIPTION</span></span>
<span data-ttu-id="88f14-106">Új csomópont-típus felvétele meglévő fürtbe.</span><span class="sxs-lookup"><span data-stu-id="88f14-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="88f14-107">Példák</span><span class="sxs-lookup"><span data-stu-id="88f14-107">EXAMPLES</span></span>

### <span data-ttu-id="88f14-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="88f14-108">Example 1</span></span>
```powershell
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="88f14-109">A parancs az 5 kapacitású új NodeType, a VM-rendszergazdai név pedig "adminName" nevet ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="88f14-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="88f14-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88f14-110">PARAMETERS</span></span>

### <span data-ttu-id="88f14-111">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="88f14-111">-Capacity</span></span>
<span data-ttu-id="88f14-112">Kapacitás</span><span class="sxs-lookup"><span data-stu-id="88f14-112">Capacity</span></span>

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

### <span data-ttu-id="88f14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88f14-113">-DefaultProfile</span></span>
<span data-ttu-id="88f14-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88f14-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88f14-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="88f14-115">-DurabilityLevel</span></span>
<span data-ttu-id="88f14-116">Adja meg a NodeType tartóssági szintjét.</span><span class="sxs-lookup"><span data-stu-id="88f14-116">Specify the durability level of the NodeType.</span></span>

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

### <span data-ttu-id="88f14-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="88f14-117">-Name</span></span>
<span data-ttu-id="88f14-118">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="88f14-118">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="88f14-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="88f14-119">-NodeType</span></span>
<span data-ttu-id="88f14-120">A csomópont típusa név</span><span class="sxs-lookup"><span data-stu-id="88f14-120">The node type name</span></span>

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

### <span data-ttu-id="88f14-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88f14-121">-ResourceGroupName</span></span>
<span data-ttu-id="88f14-122">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="88f14-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="88f14-123">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="88f14-123">-Tier</span></span>
<span data-ttu-id="88f14-124">VM SKU Tier</span><span class="sxs-lookup"><span data-stu-id="88f14-124">Vm Sku Tier</span></span>

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

### <span data-ttu-id="88f14-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="88f14-125">-VmPassword</span></span>
<span data-ttu-id="88f14-126">A VM-be való bejelentkezés jelszava</span><span class="sxs-lookup"><span data-stu-id="88f14-126">The password for login to the Vm</span></span>

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

### <span data-ttu-id="88f14-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="88f14-127">-VmSku</span></span>
<span data-ttu-id="88f14-128">A SKU neve</span><span class="sxs-lookup"><span data-stu-id="88f14-128">The sku name</span></span>

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

### <span data-ttu-id="88f14-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="88f14-129">-VmUserName</span></span>
<span data-ttu-id="88f14-130">A VM-be való bejelentkezéshez használt Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="88f14-130">The user name for logging to Vm</span></span>

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

### <span data-ttu-id="88f14-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="88f14-131">-Confirm</span></span>
<span data-ttu-id="88f14-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="88f14-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88f14-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88f14-133">-WhatIf</span></span>
<span data-ttu-id="88f14-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="88f14-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88f14-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="88f14-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88f14-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88f14-136">CommonParameters</span></span>
<span data-ttu-id="88f14-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88f14-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88f14-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="88f14-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88f14-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88f14-139">INPUTS</span></span>

### <span data-ttu-id="88f14-140">System. String</span><span class="sxs-lookup"><span data-stu-id="88f14-140">System.String</span></span>

### <span data-ttu-id="88f14-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="88f14-141">System.Int32</span></span>

### <span data-ttu-id="88f14-142">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="88f14-142">System.Security.SecureString</span></span>

### <span data-ttu-id="88f14-143">Microsoft. Azure. Command. ServiceFabric. models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="88f14-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="88f14-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88f14-144">OUTPUTS</span></span>

### <span data-ttu-id="88f14-145">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="88f14-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="88f14-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88f14-146">NOTES</span></span>

## <span data-ttu-id="88f14-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88f14-147">RELATED LINKS</span></span>
