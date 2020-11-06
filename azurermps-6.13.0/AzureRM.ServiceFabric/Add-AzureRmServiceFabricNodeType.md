---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 573dd2f4681ae140fbe98de5d9a7e9df4e2dc764
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494901"
---
# <span data-ttu-id="26082-101">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="26082-101">Add-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="26082-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26082-102">SYNOPSIS</span></span>
<span data-ttu-id="26082-103">Új csomópont-típus felvétele a meglévő fürtbe.</span><span class="sxs-lookup"><span data-stu-id="26082-103">Add a new node type to the existing cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26082-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26082-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26082-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="26082-105">DESCRIPTION</span></span>
<span data-ttu-id="26082-106">Új csomópont-típus felvétele meglévő fürtbe.</span><span class="sxs-lookup"><span data-stu-id="26082-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="26082-107">Példák</span><span class="sxs-lookup"><span data-stu-id="26082-107">EXAMPLES</span></span>

### <span data-ttu-id="26082-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="26082-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="26082-109">A parancs az 5 kapacitású új NodeType, a VM-rendszergazdai név pedig "adminName" nevet ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="26082-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="26082-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26082-110">PARAMETERS</span></span>

### <span data-ttu-id="26082-111">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="26082-111">-Capacity</span></span>
<span data-ttu-id="26082-112">Kapacitás</span><span class="sxs-lookup"><span data-stu-id="26082-112">Capacity</span></span>

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

### <span data-ttu-id="26082-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26082-113">-DefaultProfile</span></span>
<span data-ttu-id="26082-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26082-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26082-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="26082-115">-DurabilityLevel</span></span>
<span data-ttu-id="26082-116">Adja meg a NodeType tartóssági szintjét.</span><span class="sxs-lookup"><span data-stu-id="26082-116">Specify the durability level of the NodeType.</span></span>

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

### <span data-ttu-id="26082-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="26082-117">-Name</span></span>
<span data-ttu-id="26082-118">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="26082-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="26082-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="26082-119">-NodeType</span></span>
<span data-ttu-id="26082-120">A csomópont típusa név.</span><span class="sxs-lookup"><span data-stu-id="26082-120">The node type name.</span></span>

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

### <span data-ttu-id="26082-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26082-121">-ResourceGroupName</span></span>
<span data-ttu-id="26082-122">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="26082-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="26082-123">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="26082-123">-Tier</span></span>
<span data-ttu-id="26082-124">VM SKU Tier.</span><span class="sxs-lookup"><span data-stu-id="26082-124">Vm Sku Tier.</span></span>

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

### <span data-ttu-id="26082-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="26082-125">-VmPassword</span></span>
<span data-ttu-id="26082-126">A VM-be való bejelentkezés jelszava.</span><span class="sxs-lookup"><span data-stu-id="26082-126">The password of login to the Vm.</span></span>

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

### <span data-ttu-id="26082-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="26082-127">-VmSku</span></span>
<span data-ttu-id="26082-128">A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="26082-128">The sku name.</span></span>

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

### <span data-ttu-id="26082-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="26082-129">-VmUserName</span></span>
<span data-ttu-id="26082-130">Felhasználónév a VM-be való bejelentkezéshez.</span><span class="sxs-lookup"><span data-stu-id="26082-130">The user name for login to Vm.</span></span>

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

### <span data-ttu-id="26082-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="26082-131">-Confirm</span></span>
<span data-ttu-id="26082-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="26082-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26082-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26082-133">-WhatIf</span></span>
<span data-ttu-id="26082-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="26082-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26082-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="26082-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26082-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26082-136">CommonParameters</span></span>
<span data-ttu-id="26082-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="26082-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26082-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26082-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26082-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26082-139">INPUTS</span></span>

### <span data-ttu-id="26082-140">System. String</span><span class="sxs-lookup"><span data-stu-id="26082-140">System.String</span></span>
<span data-ttu-id="26082-141">Paraméterek: NodeType (ByValue), Tier (ByValue), VmSku (ByValue), VmUserName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="26082-141">Parameters: NodeType (ByValue), Tier (ByValue), VmSku (ByValue), VmUserName (ByValue)</span></span>

### <span data-ttu-id="26082-142">System. Int32</span><span class="sxs-lookup"><span data-stu-id="26082-142">System.Int32</span></span>
<span data-ttu-id="26082-143">Paraméterek: kapacitás (ByValue)</span><span class="sxs-lookup"><span data-stu-id="26082-143">Parameters: Capacity (ByValue)</span></span>

### <span data-ttu-id="26082-144">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="26082-144">System.Security.SecureString</span></span>
<span data-ttu-id="26082-145">Paraméterek: VmPassword (ByValue)</span><span class="sxs-lookup"><span data-stu-id="26082-145">Parameters: VmPassword (ByValue)</span></span>

### <span data-ttu-id="26082-146">Microsoft. Azure. Command. ServiceFabric. models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="26082-146">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="26082-147">Paraméterek: DurabilityLevel (ByValue)</span><span class="sxs-lookup"><span data-stu-id="26082-147">Parameters: DurabilityLevel (ByValue)</span></span>

## <span data-ttu-id="26082-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26082-148">OUTPUTS</span></span>

### <span data-ttu-id="26082-149">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="26082-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="26082-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26082-150">NOTES</span></span>

## <span data-ttu-id="26082-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26082-151">RELATED LINKS</span></span>
