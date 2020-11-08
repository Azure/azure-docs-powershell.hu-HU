---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: 422eb25456beb57ed6ab029fa5d70a47061ca491
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187778"
---
# <span data-ttu-id="27858-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="27858-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="27858-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27858-102">SYNOPSIS</span></span>
<span data-ttu-id="27858-103">Létrehoz egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="27858-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="27858-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27858-104">SYNTAX</span></span>

### <span data-ttu-id="27858-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="27858-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27858-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="27858-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27858-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="27858-107">DESCRIPTION</span></span>
<span data-ttu-id="27858-108">A megadott IotHub kulcsát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="27858-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="27858-109">A saját nevek nem egyediek, és körültekintően kell kezelni őket.</span><span class="sxs-lookup"><span data-stu-id="27858-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="27858-110">Példák</span><span class="sxs-lookup"><span data-stu-id="27858-110">EXAMPLES</span></span>

### <span data-ttu-id="27858-111">Példa 1 kulcs felvétele egy IotHub</span><span class="sxs-lookup"><span data-stu-id="27858-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="27858-112">A iothub "myiothub" nevű "Mykey" nevű kulcs létrehozása RegistryRead engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="27858-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="27858-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27858-113">PARAMETERS</span></span>

### <span data-ttu-id="27858-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27858-114">-DefaultProfile</span></span>
<span data-ttu-id="27858-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="27858-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27858-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="27858-116">-HubId</span></span>
<span data-ttu-id="27858-117">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="27858-117">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27858-118">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="27858-118">-KeyName</span></span>
<span data-ttu-id="27858-119">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="27858-119">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27858-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="27858-120">-Name</span></span>
<span data-ttu-id="27858-121">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="27858-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27858-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="27858-122">-PrimaryKey</span></span>
<span data-ttu-id="27858-123">Az elsődleges kulcs</span><span class="sxs-lookup"><span data-stu-id="27858-123">The primary key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27858-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27858-124">-ResourceGroupName</span></span>
<span data-ttu-id="27858-125">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="27858-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27858-126">– Jogok</span><span class="sxs-lookup"><span data-stu-id="27858-126">-Rights</span></span>
<span data-ttu-id="27858-127">A IOTHub engedélyei</span><span class="sxs-lookup"><span data-stu-id="27858-127">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases:
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27858-128">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="27858-128">-SecondaryKey</span></span>
<span data-ttu-id="27858-129">A másodlagos kulcs</span><span class="sxs-lookup"><span data-stu-id="27858-129">The Secondary Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27858-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="27858-130">-Confirm</span></span>
<span data-ttu-id="27858-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="27858-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27858-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27858-132">-WhatIf</span></span>
<span data-ttu-id="27858-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="27858-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27858-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="27858-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27858-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27858-135">CommonParameters</span></span>
<span data-ttu-id="27858-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27858-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27858-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27858-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27858-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27858-138">INPUTS</span></span>

### <span data-ttu-id="27858-139">System. String</span><span class="sxs-lookup"><span data-stu-id="27858-139">System.String</span></span>

## <span data-ttu-id="27858-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27858-140">OUTPUTS</span></span>

### <span data-ttu-id="27858-141">Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="27858-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="27858-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27858-142">NOTES</span></span>

## <span data-ttu-id="27858-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27858-143">RELATED LINKS</span></span>
