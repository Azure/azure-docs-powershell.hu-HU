---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: cc843ca942ae79fe76e1dd50e76c876e4d05b5ac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187738"
---
# <span data-ttu-id="df451-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="df451-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="df451-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df451-102">SYNOPSIS</span></span>
<span data-ttu-id="df451-103">Azure IoT hub-kulcs létrehozása</span><span class="sxs-lookup"><span data-stu-id="df451-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="df451-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df451-104">SYNTAX</span></span>

### <span data-ttu-id="df451-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df451-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df451-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="df451-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df451-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="df451-107">DESCRIPTION</span></span>
<span data-ttu-id="df451-108">Azure IoT hub-kulcs létrehozása</span><span class="sxs-lookup"><span data-stu-id="df451-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="df451-109">Példák</span><span class="sxs-lookup"><span data-stu-id="df451-109">EXAMPLES</span></span>

### <span data-ttu-id="df451-110">Példa 1 az elsődleges kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="df451-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="df451-111">Az Azure IOT-hub "testKey" engedélyezési házirendjének regenerált elsődleges kulcsa.</span><span class="sxs-lookup"><span data-stu-id="df451-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="df451-112">2. példa kulcsok cseréje</span><span class="sxs-lookup"><span data-stu-id="df451-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="df451-113">Az Azure IOT-hub "testKey" engedélyezési házirendjének swapping billentyűi.</span><span class="sxs-lookup"><span data-stu-id="df451-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="df451-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df451-114">PARAMETERS</span></span>

### <span data-ttu-id="df451-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df451-115">-DefaultProfile</span></span>
<span data-ttu-id="df451-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="df451-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df451-117">-HubId</span><span class="sxs-lookup"><span data-stu-id="df451-117">-HubId</span></span>
<span data-ttu-id="df451-118">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="df451-118">IotHub Resource Id</span></span>

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

### <span data-ttu-id="df451-119">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="df451-119">-KeyName</span></span>
<span data-ttu-id="df451-120">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="df451-120">Name of the Key</span></span>

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

### <span data-ttu-id="df451-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="df451-121">-Name</span></span>
<span data-ttu-id="df451-122">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="df451-122">Name of the IotHub</span></span>

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

### <span data-ttu-id="df451-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="df451-123">-RenewKey</span></span>
<span data-ttu-id="df451-124">A kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="df451-124">Regenerate Key.</span></span>

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

### <span data-ttu-id="df451-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df451-125">-ResourceGroupName</span></span>
<span data-ttu-id="df451-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="df451-126">Resource Group Name</span></span>

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

### <span data-ttu-id="df451-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="df451-127">-Confirm</span></span>
<span data-ttu-id="df451-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="df451-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df451-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df451-129">-WhatIf</span></span>
<span data-ttu-id="df451-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="df451-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df451-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df451-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df451-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df451-132">CommonParameters</span></span>
<span data-ttu-id="df451-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df451-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df451-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df451-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df451-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df451-135">INPUTS</span></span>

### <span data-ttu-id="df451-136">System. String</span><span class="sxs-lookup"><span data-stu-id="df451-136">System.String</span></span>

## <span data-ttu-id="df451-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df451-137">OUTPUTS</span></span>

### <span data-ttu-id="df451-138">Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="df451-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="df451-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df451-139">NOTES</span></span>

## <span data-ttu-id="df451-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df451-140">RELATED LINKS</span></span>
