---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: fe964ba2672c67fc9bb5e47e7b7a16d4fdd49471
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942505"
---
# <span data-ttu-id="82f00-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="82f00-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="82f00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82f00-102">SYNOPSIS</span></span>
<span data-ttu-id="82f00-103">Létrehoz egy IotHub-kulcsot.</span><span class="sxs-lookup"><span data-stu-id="82f00-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="82f00-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="82f00-104">SYNTAX</span></span>

### <span data-ttu-id="82f00-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="82f00-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82f00-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="82f00-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82f00-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="82f00-107">DESCRIPTION</span></span>
<span data-ttu-id="82f00-108">Létrehoz egy kulcsot a megadott IotHubhoz.</span><span class="sxs-lookup"><span data-stu-id="82f00-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="82f00-109">A Kulcsnevek nem egyediek, ezért gondosan kell kezelni őket.</span><span class="sxs-lookup"><span data-stu-id="82f00-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="82f00-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="82f00-110">EXAMPLES</span></span>

### <span data-ttu-id="82f00-111">1. példa: Kulcs hozzáadása iotHubhoz</span><span class="sxs-lookup"><span data-stu-id="82f00-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="82f00-112">Létrehoz egy "mykey" nevű kulcsot a RegistryRead engedélyekkel rendelkező iothub "myiothub" számára.</span><span class="sxs-lookup"><span data-stu-id="82f00-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="82f00-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82f00-113">PARAMETERS</span></span>

### <span data-ttu-id="82f00-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82f00-114">-DefaultProfile</span></span>
<span data-ttu-id="82f00-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="82f00-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82f00-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="82f00-116">-HubId</span></span>
<span data-ttu-id="82f00-117">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="82f00-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="82f00-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="82f00-118">-KeyName</span></span>
<span data-ttu-id="82f00-119">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="82f00-119">Name of the Key</span></span>

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

### <span data-ttu-id="82f00-120">-Name</span><span class="sxs-lookup"><span data-stu-id="82f00-120">-Name</span></span>
<span data-ttu-id="82f00-121">Az IotHub neve</span><span class="sxs-lookup"><span data-stu-id="82f00-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="82f00-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="82f00-122">-PrimaryKey</span></span>
<span data-ttu-id="82f00-123">Az elsődleges kulcs</span><span class="sxs-lookup"><span data-stu-id="82f00-123">The primary key</span></span>

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

### <span data-ttu-id="82f00-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82f00-124">-ResourceGroupName</span></span>
<span data-ttu-id="82f00-125">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="82f00-125">Resource Group Name</span></span>

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

### <span data-ttu-id="82f00-126">-Rights</span><span class="sxs-lookup"><span data-stu-id="82f00-126">-Rights</span></span>
<span data-ttu-id="82f00-127">Az IOTHub engedélyeinek</span><span class="sxs-lookup"><span data-stu-id="82f00-127">The permissions for this IOTHub</span></span>

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

### <span data-ttu-id="82f00-128">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="82f00-128">-SecondaryKey</span></span>
<span data-ttu-id="82f00-129">A másodlagos kulcs</span><span class="sxs-lookup"><span data-stu-id="82f00-129">The Secondary Key</span></span>

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

### <span data-ttu-id="82f00-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82f00-130">-Confirm</span></span>
<span data-ttu-id="82f00-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="82f00-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82f00-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82f00-132">-WhatIf</span></span>
<span data-ttu-id="82f00-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="82f00-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82f00-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="82f00-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82f00-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82f00-135">CommonParameters</span></span>
<span data-ttu-id="82f00-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82f00-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82f00-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82f00-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82f00-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82f00-138">INPUTS</span></span>

### <span data-ttu-id="82f00-139">System.String</span><span class="sxs-lookup"><span data-stu-id="82f00-139">System.String</span></span>

## <span data-ttu-id="82f00-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82f00-140">OUTPUTS</span></span>

### <span data-ttu-id="82f00-141">Microsoft.Azure.Commands.Management.iotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="82f00-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="82f00-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="82f00-142">NOTES</span></span>

## <span data-ttu-id="82f00-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82f00-143">RELATED LINKS</span></span>
