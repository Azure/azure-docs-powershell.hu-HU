---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: 7dd27544e3304570cf3fbdae861b21eabd300c35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927105"
---
# <span data-ttu-id="46d89-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="46d89-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="46d89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46d89-102">SYNOPSIS</span></span>
<span data-ttu-id="46d89-103">Azure IoT-központ kulcs létrehozása</span><span class="sxs-lookup"><span data-stu-id="46d89-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="46d89-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="46d89-104">SYNTAX</span></span>

### <span data-ttu-id="46d89-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="46d89-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46d89-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="46d89-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46d89-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="46d89-107">DESCRIPTION</span></span>
<span data-ttu-id="46d89-108">Azure IoT-központ kulcs létrehozása</span><span class="sxs-lookup"><span data-stu-id="46d89-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="46d89-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="46d89-109">EXAMPLES</span></span>

### <span data-ttu-id="46d89-110">1. példa: Az elsődleges kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="46d89-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="46d89-111">Az Azure iot-központ "testKey" engedélyezési házirendje által újragenerált elsődleges kulcs.</span><span class="sxs-lookup"><span data-stu-id="46d89-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="46d89-112">2. példa a billentyűk felcserélésére</span><span class="sxs-lookup"><span data-stu-id="46d89-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="46d89-113">Kulcsok felcserélése egy Azure iot-központ "testKey" engedélyezési házirendjére.</span><span class="sxs-lookup"><span data-stu-id="46d89-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="46d89-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46d89-114">PARAMETERS</span></span>

### <span data-ttu-id="46d89-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d89-115">-DefaultProfile</span></span>
<span data-ttu-id="46d89-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="46d89-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46d89-117">-HubId</span><span class="sxs-lookup"><span data-stu-id="46d89-117">-HubId</span></span>
<span data-ttu-id="46d89-118">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="46d89-118">IotHub Resource Id</span></span>

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

### <span data-ttu-id="46d89-119">-KeyName</span><span class="sxs-lookup"><span data-stu-id="46d89-119">-KeyName</span></span>
<span data-ttu-id="46d89-120">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="46d89-120">Name of the Key</span></span>

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

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46d89-121">-Name</span><span class="sxs-lookup"><span data-stu-id="46d89-121">-Name</span></span>
<span data-ttu-id="46d89-122">Az IotHub neve</span><span class="sxs-lookup"><span data-stu-id="46d89-122">Name of the IotHub</span></span>

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

### <span data-ttu-id="46d89-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="46d89-123">-RenewKey</span></span>
<span data-ttu-id="46d89-124">A kulcs újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="46d89-124">Regenerate Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d89-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46d89-125">-ResourceGroupName</span></span>
<span data-ttu-id="46d89-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="46d89-126">Resource Group Name</span></span>

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

### <span data-ttu-id="46d89-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46d89-127">-Confirm</span></span>
<span data-ttu-id="46d89-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="46d89-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46d89-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46d89-129">-WhatIf</span></span>
<span data-ttu-id="46d89-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="46d89-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46d89-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="46d89-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46d89-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d89-132">CommonParameters</span></span>
<span data-ttu-id="46d89-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46d89-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d89-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46d89-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d89-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46d89-135">INPUTS</span></span>

### <span data-ttu-id="46d89-136">System.String</span><span class="sxs-lookup"><span data-stu-id="46d89-136">System.String</span></span>

## <span data-ttu-id="46d89-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46d89-137">OUTPUTS</span></span>

### <span data-ttu-id="46d89-138">Microsoft.Azure.Commands.Management.iotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="46d89-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="46d89-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="46d89-139">NOTES</span></span>

## <span data-ttu-id="46d89-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46d89-140">RELATED LINKS</span></span>
