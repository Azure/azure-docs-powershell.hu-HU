---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: 422eb25456beb57ed6ab029fa5d70a47061ca491
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155483"
---
# <span data-ttu-id="1a271-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="1a271-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="1a271-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a271-102">SYNOPSIS</span></span>
<span data-ttu-id="1a271-103">Létrehoz egy IotHub-kulcsot.</span><span class="sxs-lookup"><span data-stu-id="1a271-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="1a271-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1a271-104">SYNTAX</span></span>

### <span data-ttu-id="1a271-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1a271-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a271-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1a271-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a271-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1a271-107">DESCRIPTION</span></span>
<span data-ttu-id="1a271-108">Létrehoz egy kulcsot a megadott IotHubhoz.</span><span class="sxs-lookup"><span data-stu-id="1a271-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="1a271-109">A Kulcsnevek nem egyediek, ezért gondosan kell kezelni őket.</span><span class="sxs-lookup"><span data-stu-id="1a271-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="1a271-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1a271-110">EXAMPLES</span></span>

### <span data-ttu-id="1a271-111">1. példa: Kulcs hozzáadása iotHubhoz</span><span class="sxs-lookup"><span data-stu-id="1a271-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="1a271-112">Létrehoz egy "mykey" nevű kulcsot a RegistryRead engedélyekkel rendelkező iothub "myiothub" számára.</span><span class="sxs-lookup"><span data-stu-id="1a271-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="1a271-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a271-113">PARAMETERS</span></span>

### <span data-ttu-id="1a271-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a271-114">-DefaultProfile</span></span>
<span data-ttu-id="1a271-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1a271-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a271-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="1a271-116">-HubId</span></span>
<span data-ttu-id="1a271-117">IotHub erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="1a271-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1a271-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="1a271-118">-KeyName</span></span>
<span data-ttu-id="1a271-119">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="1a271-119">Name of the Key</span></span>

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

### <span data-ttu-id="1a271-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1a271-120">-Name</span></span>
<span data-ttu-id="1a271-121">Az IotHub neve</span><span class="sxs-lookup"><span data-stu-id="1a271-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="1a271-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="1a271-122">-PrimaryKey</span></span>
<span data-ttu-id="1a271-123">Az elsődleges kulcs</span><span class="sxs-lookup"><span data-stu-id="1a271-123">The primary key</span></span>

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

### <span data-ttu-id="1a271-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a271-124">-ResourceGroupName</span></span>
<span data-ttu-id="1a271-125">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="1a271-125">Resource Group Name</span></span>

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

### <span data-ttu-id="1a271-126">-Rights</span><span class="sxs-lookup"><span data-stu-id="1a271-126">-Rights</span></span>
<span data-ttu-id="1a271-127">Az IOTHub engedélyeinek</span><span class="sxs-lookup"><span data-stu-id="1a271-127">The permissions for this IOTHub</span></span>

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

### <span data-ttu-id="1a271-128">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="1a271-128">-SecondaryKey</span></span>
<span data-ttu-id="1a271-129">A másodlagos kulcs</span><span class="sxs-lookup"><span data-stu-id="1a271-129">The Secondary Key</span></span>

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

### <span data-ttu-id="1a271-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a271-130">-Confirm</span></span>
<span data-ttu-id="1a271-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1a271-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a271-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a271-132">-WhatIf</span></span>
<span data-ttu-id="1a271-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1a271-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a271-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1a271-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a271-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a271-135">CommonParameters</span></span>
<span data-ttu-id="1a271-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a271-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a271-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a271-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a271-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a271-138">INPUTS</span></span>

### <span data-ttu-id="1a271-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1a271-139">System.String</span></span>

## <span data-ttu-id="1a271-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a271-140">OUTPUTS</span></span>

### <span data-ttu-id="1a271-141">Microsoft.Azure.Commands.Management.iotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1a271-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="1a271-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1a271-142">NOTES</span></span>

## <span data-ttu-id="1a271-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a271-143">RELATED LINKS</span></span>
