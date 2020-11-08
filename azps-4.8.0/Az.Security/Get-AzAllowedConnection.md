---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzAllowedConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
ms.openlocfilehash: 3a604cbdda30612016763fef75fcf62e0c8e36f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024471"
---
# <span data-ttu-id="d07a7-101">Get-AzAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="d07a7-101">Get-AzAllowedConnection</span></span>

## <span data-ttu-id="d07a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d07a7-102">SYNOPSIS</span></span>
<span data-ttu-id="d07a7-103">Az előfizetés erőforrásai között engedélyezett forgalom megjelenítésére szolgál</span><span class="sxs-lookup"><span data-stu-id="d07a7-103">Used to display allowed traffic between resources for the subscription</span></span>


## <span data-ttu-id="d07a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d07a7-104">SYNTAX</span></span>

### <span data-ttu-id="d07a7-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d07a7-105">SubscriptionScope (Default)</span></span>
```
Get-AzAllowedConnection [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d07a7-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="d07a7-106">ResourceGroupLevelResource</span></span>
```
Get-AzAllowedConnection -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d07a7-107">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d07a7-107">-ResourceId</span></span>
```
Get-AzAllowedConnection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d07a7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d07a7-108">DESCRIPTION</span></span>
<span data-ttu-id="d07a7-109">Beolvassa az előfizetés és a hely erőforrásai közötti esetleges forgalmat a kapcsolat típusa alapján.</span><span class="sxs-lookup"><span data-stu-id="d07a7-109">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="d07a7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d07a7-110">EXAMPLES</span></span>

### <span data-ttu-id="d07a7-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d07a7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAllowedConnection
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/virtualMachines
Name:   Internal
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

### <span data-ttu-id="d07a7-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="d07a7-112">Example 2</span></span>
```powershell
PS C:\> Get-AzAllowedConnection -ResourceGroupName "myService1" -Location "centralus" -Name "Internal"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/Internal
Name:   virtualMachines
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="d07a7-113">Beolvassa az előfizetés és a hely erőforrásai közötti esetleges forgalmat a kapcsolat típusa alapján.</span><span class="sxs-lookup"><span data-stu-id="d07a7-113">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="d07a7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d07a7-114">PARAMETERS</span></span>

### <span data-ttu-id="d07a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d07a7-115">-DefaultProfile</span></span>
<span data-ttu-id="d07a7-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d07a7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d07a7-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="d07a7-117">-Location</span></span>
<span data-ttu-id="d07a7-118">Helyre.</span><span class="sxs-lookup"><span data-stu-id="d07a7-118">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07a7-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d07a7-119">-Name</span></span>
<span data-ttu-id="d07a7-120">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="d07a7-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07a7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d07a7-121">-ResourceGroupName</span></span>
<span data-ttu-id="d07a7-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d07a7-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07a7-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d07a7-123">-ResourceId</span></span>
<span data-ttu-id="d07a7-124">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="d07a7-124">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d07a7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d07a7-125">CommonParameters</span></span>
<span data-ttu-id="d07a7-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d07a7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d07a7-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d07a7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d07a7-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d07a7-128">INPUTS</span></span>

### <span data-ttu-id="d07a7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d07a7-129">System.String</span></span>

## <span data-ttu-id="d07a7-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d07a7-130">OUTPUTS</span></span>

### <span data-ttu-id="d07a7-131">Microsoft. Azure. commands. Security. models. AllowedConnection. PSSecurityAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="d07a7-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span></span>


## <span data-ttu-id="d07a7-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d07a7-132">NOTES</span></span>

## <span data-ttu-id="d07a7-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d07a7-133">RELATED LINKS</span></span>
