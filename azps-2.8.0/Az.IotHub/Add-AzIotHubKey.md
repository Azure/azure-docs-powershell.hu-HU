---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: 3505a2b18ac35644fe401dea4aca8c96b10a7f2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666295"
---
# <span data-ttu-id="10b76-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="10b76-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="10b76-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10b76-102">SYNOPSIS</span></span>
<span data-ttu-id="10b76-103">Létrehoz egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="10b76-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="10b76-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10b76-104">SYNTAX</span></span>

### <span data-ttu-id="10b76-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="10b76-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10b76-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="10b76-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10b76-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="10b76-107">DESCRIPTION</span></span>
<span data-ttu-id="10b76-108">A megadott IotHub kulcsát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="10b76-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="10b76-109">A saját nevek nem egyediek, és körültekintően kell kezelni őket.</span><span class="sxs-lookup"><span data-stu-id="10b76-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="10b76-110">Példák</span><span class="sxs-lookup"><span data-stu-id="10b76-110">EXAMPLES</span></span>

### <span data-ttu-id="10b76-111">Példa 1 kulcs felvétele egy IotHub</span><span class="sxs-lookup"><span data-stu-id="10b76-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="10b76-112">A iothub "myiothub" nevű "Mykey" nevű kulcs létrehozása RegistryRead engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="10b76-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="10b76-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10b76-113">PARAMETERS</span></span>

### <span data-ttu-id="10b76-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10b76-114">-DefaultProfile</span></span>
<span data-ttu-id="10b76-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="10b76-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10b76-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="10b76-116">-HubId</span></span>
<span data-ttu-id="10b76-117">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="10b76-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="10b76-118">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="10b76-118">-KeyName</span></span>
<span data-ttu-id="10b76-119">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="10b76-119">Name of the Key</span></span>

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

### <span data-ttu-id="10b76-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="10b76-120">-Name</span></span>
<span data-ttu-id="10b76-121">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="10b76-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="10b76-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="10b76-122">-PrimaryKey</span></span>
<span data-ttu-id="10b76-123">Az elsődleges kulcs</span><span class="sxs-lookup"><span data-stu-id="10b76-123">The primary key</span></span>

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

### <span data-ttu-id="10b76-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10b76-124">-ResourceGroupName</span></span>
<span data-ttu-id="10b76-125">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="10b76-125">Resource Group Name</span></span>

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

### <span data-ttu-id="10b76-126">– Jogok</span><span class="sxs-lookup"><span data-stu-id="10b76-126">-Rights</span></span>
<span data-ttu-id="10b76-127">A IOTHub engedélyei</span><span class="sxs-lookup"><span data-stu-id="10b76-127">The permissions for this IOTHub</span></span>

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

### <span data-ttu-id="10b76-128">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="10b76-128">-SecondaryKey</span></span>
<span data-ttu-id="10b76-129">A másodlagos kulcs</span><span class="sxs-lookup"><span data-stu-id="10b76-129">The Secondary Key</span></span>

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

### <span data-ttu-id="10b76-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="10b76-130">-Confirm</span></span>
<span data-ttu-id="10b76-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="10b76-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10b76-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10b76-132">-WhatIf</span></span>
<span data-ttu-id="10b76-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="10b76-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10b76-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="10b76-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10b76-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10b76-135">CommonParameters</span></span>
<span data-ttu-id="10b76-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10b76-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10b76-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10b76-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10b76-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10b76-138">INPUTS</span></span>

### <span data-ttu-id="10b76-139">System. String</span><span class="sxs-lookup"><span data-stu-id="10b76-139">System.String</span></span>

## <span data-ttu-id="10b76-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10b76-140">OUTPUTS</span></span>

### <span data-ttu-id="10b76-141">Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="10b76-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="10b76-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10b76-142">NOTES</span></span>

## <span data-ttu-id="10b76-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10b76-143">RELATED LINKS</span></span>
