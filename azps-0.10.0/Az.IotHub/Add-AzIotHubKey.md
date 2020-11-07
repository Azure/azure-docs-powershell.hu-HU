---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: 75f623890963095efbf37a631bf4c0736245fe28
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843977"
---
# <span data-ttu-id="b4a36-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="b4a36-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="b4a36-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4a36-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a36-103">Létrehoz egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="b4a36-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="b4a36-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4a36-104">SYNTAX</span></span>

### <span data-ttu-id="b4a36-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b4a36-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4a36-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b4a36-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4a36-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4a36-107">DESCRIPTION</span></span>
<span data-ttu-id="b4a36-108">A megadott IotHub kulcsát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="b4a36-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="b4a36-109">A saját nevek nem egyediek, és körültekintően kell kezelni őket.</span><span class="sxs-lookup"><span data-stu-id="b4a36-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="b4a36-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b4a36-110">EXAMPLES</span></span>

### <span data-ttu-id="b4a36-111">Példa 1 kulcs felvétele egy IotHub</span><span class="sxs-lookup"><span data-stu-id="b4a36-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="b4a36-112">A iothub "myiothub" nevű "Mykey" nevű kulcs létrehozása RegistryRead engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="b4a36-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="b4a36-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4a36-113">PARAMETERS</span></span>

### <span data-ttu-id="b4a36-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4a36-114">-DefaultProfile</span></span>
<span data-ttu-id="b4a36-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b4a36-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4a36-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="b4a36-116">-HubId</span></span>
<span data-ttu-id="b4a36-117">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="b4a36-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b4a36-118">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="b4a36-118">-KeyName</span></span>
<span data-ttu-id="b4a36-119">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="b4a36-119">Name of the Key</span></span>

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

### <span data-ttu-id="b4a36-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b4a36-120">-Name</span></span>
<span data-ttu-id="b4a36-121">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="b4a36-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="b4a36-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="b4a36-122">-PrimaryKey</span></span>
<span data-ttu-id="b4a36-123">Az elsődleges kulcs</span><span class="sxs-lookup"><span data-stu-id="b4a36-123">The primary key</span></span>

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

### <span data-ttu-id="b4a36-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4a36-124">-ResourceGroupName</span></span>
<span data-ttu-id="b4a36-125">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="b4a36-125">Resource Group Name</span></span>

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

### <span data-ttu-id="b4a36-126">– Jogok</span><span class="sxs-lookup"><span data-stu-id="b4a36-126">-Rights</span></span>
<span data-ttu-id="b4a36-127">A IOTHub engedélyei</span><span class="sxs-lookup"><span data-stu-id="b4a36-127">The permissions for this IOTHub</span></span>

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

### <span data-ttu-id="b4a36-128">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="b4a36-128">-SecondaryKey</span></span>
<span data-ttu-id="b4a36-129">A másodlagos kulcs</span><span class="sxs-lookup"><span data-stu-id="b4a36-129">The Secondary Key</span></span>

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

### <span data-ttu-id="b4a36-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b4a36-130">-Confirm</span></span>
<span data-ttu-id="b4a36-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b4a36-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4a36-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4a36-132">-WhatIf</span></span>
<span data-ttu-id="b4a36-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b4a36-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4a36-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b4a36-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4a36-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4a36-135">CommonParameters</span></span>
<span data-ttu-id="b4a36-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4a36-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4a36-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4a36-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4a36-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4a36-138">INPUTS</span></span>

### <span data-ttu-id="b4a36-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b4a36-139">System.String</span></span>

## <span data-ttu-id="b4a36-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4a36-140">OUTPUTS</span></span>

### <span data-ttu-id="b4a36-141">Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b4a36-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="b4a36-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4a36-142">NOTES</span></span>

## <span data-ttu-id="b4a36-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4a36-143">RELATED LINKS</span></span>
