---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
ms.openlocfilehash: 52fae225184b83675f21af941fa125576252ffbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014886"
---
# <span data-ttu-id="90051-101">Get-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="90051-101">Get-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="90051-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90051-102">SYNOPSIS</span></span>
<span data-ttu-id="90051-103">Eszközbiztonsági csoport (IoT-központ biztonság)</span><span class="sxs-lookup"><span data-stu-id="90051-103">Get device security group (IoT Hub security)</span></span>

## <span data-ttu-id="90051-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="90051-104">SYNTAX</span></span>

### <span data-ttu-id="90051-105">ResourceIdScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="90051-105">ResourceIdScope (Default)</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="90051-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="90051-106">ResourceIdLevelResource</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90051-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="90051-107">DESCRIPTION</span></span>
<span data-ttu-id="90051-108">A Get-AzDeviceSecurityGroup parancsmag az iot biztonsági megoldásban definiált eszközbiztonsági csoportot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="90051-108">The Get-AzDeviceSecurityGroup cmdlet returns a device security group defined in iot security solution</span></span>

## <span data-ttu-id="90051-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="90051-109">EXAMPLES</span></span>

### <span data-ttu-id="90051-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="90051-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" -Name "MySecurityGroup" 

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub/providers/Microsoft.Security/deviceSecurityGroups/MySecurityGroup"
Name: "MySecurityGroup"
Type: "Microsoft.Security/deviceSecurityGroups"
ThresholdRules: []
TimeWindowRules: [
            {
              RuleType: "ActiveConnectionsNotInAllowedRange"
              DisplayName: "Number of active connections is not in allowed range"
              Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
            }
            {
              RuleType: "AmqpC2DMessagesNotInAllowedRange"
              DisplayName: "Number of cloud to device messages (AMQP protocol) is not in allowed range"
              Description: "Get an alert when the number of cloud to device messages (AMQP protocol) in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
            }]
AllowlistRules: [
            {
              RuleType": "ConnectionToIpNotAllowed",
              DisplayName: "Outbound connection to an ip that isn't allowed"
              Description: "Get an alert when an outbound connection is created between your device and an ip that isn't allowed"
              IsEnabled: false
              ValueType: "IpCidr"
              AllowlistValues: []
            },
            {
              RuleType: "LocalUserNotAllowed"
              DisplayName: "Login by a local user that isn't allowed"
              Description: "Get an alert when a local user that isn't allowed logins to the device"
              IsEnabled: false
              ValueType: "String"
              AllowlistValues: []
            }]
DenylistRules: []
```

<span data-ttu-id="90051-111">A MySecurityGroup eszközbiztonsági csoport lekérte az IoT Hubon a következő újraforrásazonosítóval: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="90051-111">Get device security group "MySecurityGroup" in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

### <span data-ttu-id="90051-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="90051-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 

Array of security group items like the item returned in example 1
```

<span data-ttu-id="90051-113">Eszközbiztonsági csoport az IoT-központban a következő újraforrásazonosítóval: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="90051-113">Get list of device security group in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="90051-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90051-114">PARAMETERS</span></span>

### <span data-ttu-id="90051-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90051-115">-DefaultProfile</span></span>
<span data-ttu-id="90051-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="90051-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90051-117">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="90051-117">-HubResourceId</span></span>
<span data-ttu-id="90051-118">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="90051-118">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90051-119">-Name</span><span class="sxs-lookup"><span data-stu-id="90051-119">-Name</span></span>
<span data-ttu-id="90051-120">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="90051-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90051-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90051-121">CommonParameters</span></span>
<span data-ttu-id="90051-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90051-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90051-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90051-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90051-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90051-124">INPUTS</span></span>

### <span data-ttu-id="90051-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="90051-125">None</span></span>

## <span data-ttu-id="90051-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90051-126">OUTPUTS</span></span>

### <span data-ttu-id="90051-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="90051-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="90051-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="90051-128">NOTES</span></span>

## <span data-ttu-id="90051-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90051-129">RELATED LINKS</span></span>
