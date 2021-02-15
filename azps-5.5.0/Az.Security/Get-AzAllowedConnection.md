---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzAllowedConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
ms.openlocfilehash: 3a604cbdda30612016763fef75fcf62e0c8e36f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145842"
---
# <span data-ttu-id="cf0fc-101">Get-AzAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="cf0fc-101">Get-AzAllowedConnection</span></span>

## <span data-ttu-id="cf0fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf0fc-102">SYNOPSIS</span></span>
<span data-ttu-id="cf0fc-103">Az előfizetés erőforrásai közötti engedélyezett adatforgalom megjelenítésére használható</span><span class="sxs-lookup"><span data-stu-id="cf0fc-103">Used to display allowed traffic between resources for the subscription</span></span>


## <span data-ttu-id="cf0fc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cf0fc-104">SYNTAX</span></span>

### <span data-ttu-id="cf0fc-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cf0fc-105">SubscriptionScope (Default)</span></span>
```
Get-AzAllowedConnection [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf0fc-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="cf0fc-106">ResourceGroupLevelResource</span></span>
```
Get-AzAllowedConnection -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf0fc-107">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf0fc-107">-ResourceId</span></span>
```
Get-AzAllowedConnection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf0fc-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cf0fc-108">DESCRIPTION</span></span>
<span data-ttu-id="cf0fc-109">Az előfizetés és a hely erőforrásai közötti összes lehetséges adatforgalom listáját tartalmazza a kapcsolat típusa alapján.</span><span class="sxs-lookup"><span data-stu-id="cf0fc-109">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="cf0fc-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cf0fc-110">EXAMPLES</span></span>

### <span data-ttu-id="cf0fc-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="cf0fc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAllowedConnection
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/virtualMachines
Name:   Internal
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

### <span data-ttu-id="cf0fc-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="cf0fc-112">Example 2</span></span>
```powershell
PS C:\> Get-AzAllowedConnection -ResourceGroupName "myService1" -Location "centralus" -Name "Internal"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/Internal
Name:   virtualMachines
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="cf0fc-113">A kapcsolat típusa alapján beveszi az erőforrások és a helyszín közötti összes lehetséges adatforgalmat.</span><span class="sxs-lookup"><span data-stu-id="cf0fc-113">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="cf0fc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf0fc-114">PARAMETERS</span></span>

### <span data-ttu-id="cf0fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf0fc-115">-DefaultProfile</span></span>
<span data-ttu-id="cf0fc-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf0fc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf0fc-117">-Location</span><span class="sxs-lookup"><span data-stu-id="cf0fc-117">-Location</span></span>
<span data-ttu-id="cf0fc-118">Hely.</span><span class="sxs-lookup"><span data-stu-id="cf0fc-118">Location.</span></span>

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

### <span data-ttu-id="cf0fc-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cf0fc-119">-Name</span></span>
<span data-ttu-id="cf0fc-120">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="cf0fc-120">Resource name.</span></span>

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

### <span data-ttu-id="cf0fc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf0fc-121">-ResourceGroupName</span></span>
<span data-ttu-id="cf0fc-122">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cf0fc-122">Resource group name.</span></span>

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

### <span data-ttu-id="cf0fc-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf0fc-123">-ResourceId</span></span>
<span data-ttu-id="cf0fc-124">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="cf0fc-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="cf0fc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf0fc-125">CommonParameters</span></span>
<span data-ttu-id="cf0fc-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf0fc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf0fc-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf0fc-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf0fc-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf0fc-128">INPUTS</span></span>

### <span data-ttu-id="cf0fc-129">System.String</span><span class="sxs-lookup"><span data-stu-id="cf0fc-129">System.String</span></span>

## <span data-ttu-id="cf0fc-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf0fc-130">OUTPUTS</span></span>

### <span data-ttu-id="cf0fc-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="cf0fc-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span></span>


## <span data-ttu-id="cf0fc-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cf0fc-132">NOTES</span></span>

## <span data-ttu-id="cf0fc-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf0fc-133">RELATED LINKS</span></span>
