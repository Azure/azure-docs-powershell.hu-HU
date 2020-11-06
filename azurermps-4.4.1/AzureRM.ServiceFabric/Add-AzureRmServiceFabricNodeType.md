---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 305e406a3f2ef723eb0431b495106bb688ffe61c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500695"
---
# <span data-ttu-id="ee8d0-101">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="ee8d0-101">Add-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="ee8d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee8d0-102">SYNOPSIS</span></span>
<span data-ttu-id="ee8d0-103">Új csomópont-típus felvétele a meglévő fürtbe.</span><span class="sxs-lookup"><span data-stu-id="ee8d0-103">Add a new node type to the existing cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee8d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee8d0-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -Capacity <Int32> -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee8d0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee8d0-105">DESCRIPTION</span></span>
<span data-ttu-id="ee8d0-106">Új csomópont-típus felvétele meglévő fürtbe.</span><span class="sxs-lookup"><span data-stu-id="ee8d0-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="ee8d0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ee8d0-107">EXAMPLES</span></span>

### <span data-ttu-id="ee8d0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ee8d0-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="ee8d0-109">A parancs az 5 kapacitású új NodeType, a VM-rendszergazdai név pedig "adminName" nevet ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="ee8d0-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="ee8d0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee8d0-110">PARAMETERS</span></span>

### <span data-ttu-id="ee8d0-111">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="ee8d0-111">-Capacity</span></span>
<span data-ttu-id="ee8d0-112">Kapacitás</span><span class="sxs-lookup"><span data-stu-id="ee8d0-112">Capacity</span></span>

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

### <span data-ttu-id="ee8d0-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ee8d0-113">-Name</span></span>
<span data-ttu-id="ee8d0-114">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="ee8d0-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ee8d0-115">-NodeType</span><span class="sxs-lookup"><span data-stu-id="ee8d0-115">-NodeType</span></span>
<span data-ttu-id="ee8d0-116">A csomópont típusa név.</span><span class="sxs-lookup"><span data-stu-id="ee8d0-116">The node type name.</span></span>

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

### <span data-ttu-id="ee8d0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee8d0-117">-ResourceGroupName</span></span>
<span data-ttu-id="ee8d0-118">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="ee8d0-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ee8d0-119">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="ee8d0-119">-Tier</span></span>
<span data-ttu-id="ee8d0-120">VM SKU Tier.</span><span class="sxs-lookup"><span data-stu-id="ee8d0-120">Vm Sku Tier.</span></span>

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

### <span data-ttu-id="ee8d0-121">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="ee8d0-121">-DurabilityLevel</span></span>
<span data-ttu-id="ee8d0-122">Adja meg a NodeType tartóssági szintjét.</span><span class="sxs-lookup"><span data-stu-id="ee8d0-122">Specify the durability level of the NodeType.</span></span>

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

### <span data-ttu-id="ee8d0-123">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="ee8d0-123">-VmPassword</span></span>
<span data-ttu-id="ee8d0-124">A VM-be való bejelentkezés jelszava.</span><span class="sxs-lookup"><span data-stu-id="ee8d0-124">The password of login to the Vm.</span></span>

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

### <span data-ttu-id="ee8d0-125">-VmSku</span><span class="sxs-lookup"><span data-stu-id="ee8d0-125">-VmSku</span></span>
<span data-ttu-id="ee8d0-126">A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="ee8d0-126">The sku name.</span></span>

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

### <span data-ttu-id="ee8d0-127">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="ee8d0-127">-VmUserName</span></span>
<span data-ttu-id="ee8d0-128">Felhasználónév a VM-be való bejelentkezéshez.</span><span class="sxs-lookup"><span data-stu-id="ee8d0-128">The user name for login to Vm.</span></span>

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

### <span data-ttu-id="ee8d0-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ee8d0-129">-Confirm</span></span>
<span data-ttu-id="ee8d0-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ee8d0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee8d0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee8d0-131">-WhatIf</span></span>
<span data-ttu-id="ee8d0-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ee8d0-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee8d0-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ee8d0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee8d0-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee8d0-134">-DefaultProfile</span></span>
<span data-ttu-id="ee8d0-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee8d0-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee8d0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee8d0-136">CommonParameters</span></span>
<span data-ttu-id="ee8d0-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee8d0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee8d0-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee8d0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee8d0-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee8d0-139">INPUTS</span></span>

### <span data-ttu-id="ee8d0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ee8d0-140">System.String</span></span>
<span data-ttu-id="ee8d0-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ee8d0-141">System.Int32</span></span>

## <span data-ttu-id="ee8d0-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee8d0-142">OUTPUTS</span></span>

### <span data-ttu-id="ee8d0-143">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="ee8d0-143">System.Object</span></span>

## <span data-ttu-id="ee8d0-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee8d0-144">NOTES</span></span>

## <span data-ttu-id="ee8d0-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee8d0-145">RELATED LINKS</span></span>

