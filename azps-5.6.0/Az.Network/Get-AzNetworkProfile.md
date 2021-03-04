---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
ms.openlocfilehash: f2f18ac77f923247f2bef0e78802a2f05cf302d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919882"
---
# <span data-ttu-id="e0a22-101">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e0a22-101">Get-AzNetworkProfile</span></span>

## <span data-ttu-id="e0a22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0a22-102">SYNOPSIS</span></span>
<span data-ttu-id="e0a22-103">Meglévő hálózati profil legfelső szintű erőforrást kap</span><span class="sxs-lookup"><span data-stu-id="e0a22-103">Gets an existing network profile top level resource</span></span>

## <span data-ttu-id="e0a22-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e0a22-104">SYNTAX</span></span>

### <span data-ttu-id="e0a22-105">GetByResourceNameNoExpandParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e0a22-105">GetByResourceNameNoExpandParameterSet (Default)</span></span>
```
Get-AzNetworkProfile [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0a22-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0a22-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0a22-107">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0a22-107">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0a22-108">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0a22-108">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0a22-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e0a22-109">DESCRIPTION</span></span>
<span data-ttu-id="e0a22-110">A **Get-AzNetworkProfile** parancsmag egy meglévő hálózati profil legfelső szintű erőforrását olvassa be</span><span class="sxs-lookup"><span data-stu-id="e0a22-110">The **Get-AzNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="e0a22-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e0a22-111">EXAMPLES</span></span>

### <span data-ttu-id="e0a22-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="e0a22-112">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1
```

<span data-ttu-id="e0a22-113">Ez a parancs beolvassa a hálózati profil np1-et az rg1 erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="e0a22-113">This retrieves the network profile np1 in resource group rg1</span></span>

### <span data-ttu-id="e0a22-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="e0a22-114">Example 2</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np*

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np2
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np2
```

<span data-ttu-id="e0a22-115">Ez a lekérdezés az "np" kezdetú hálózati profilokat olvassa be.</span><span class="sxs-lookup"><span data-stu-id="e0a22-115">This retrieves the network profiles that start with "np"</span></span>

## <span data-ttu-id="e0a22-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0a22-116">PARAMETERS</span></span>

### <span data-ttu-id="e0a22-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0a22-117">-DefaultProfile</span></span>
<span data-ttu-id="e0a22-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0a22-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0a22-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="e0a22-119">-ExpandResource</span></span>
<span data-ttu-id="e0a22-120">A kibontani szükséges erőforrás-hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="e0a22-120">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceIdExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0a22-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e0a22-121">-Name</span></span>
<span data-ttu-id="e0a22-122">A hálózati profil neve.</span><span class="sxs-lookup"><span data-stu-id="e0a22-122">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e0a22-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0a22-123">-ResourceGroupName</span></span>
<span data-ttu-id="e0a22-124">A hálózati profil erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="e0a22-124">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e0a22-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0a22-125">-ResourceId</span></span>
<span data-ttu-id="e0a22-126">A hálózati profil Azure-erőforrás-kezelői azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e0a22-126">The Azure resource manager id of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0a22-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0a22-127">CommonParameters</span></span>
<span data-ttu-id="e0a22-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0a22-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0a22-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0a22-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0a22-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0a22-130">INPUTS</span></span>

### <span data-ttu-id="e0a22-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e0a22-131">System.String</span></span>

## <span data-ttu-id="e0a22-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0a22-132">OUTPUTS</span></span>

### <span data-ttu-id="e0a22-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e0a22-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="e0a22-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e0a22-134">NOTES</span></span>

## <span data-ttu-id="e0a22-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0a22-135">RELATED LINKS</span></span>

[<span data-ttu-id="e0a22-136">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e0a22-136">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="e0a22-137">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e0a22-137">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="e0a22-138">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e0a22-138">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
