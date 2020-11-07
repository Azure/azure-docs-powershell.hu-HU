---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
ms.openlocfilehash: 1f57a8a9cc65ab9ff4955d6d11e6f4c1a91c417e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670539"
---
# <span data-ttu-id="b9420-101">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b9420-101">Get-AzNetworkProfile</span></span>

## <span data-ttu-id="b9420-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9420-102">SYNOPSIS</span></span>
<span data-ttu-id="b9420-103">A meglévő hálózati profil legfelső szintű erőforrását kapja</span><span class="sxs-lookup"><span data-stu-id="b9420-103">Gets an existing network profile top level resource</span></span>

## <span data-ttu-id="b9420-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9420-104">SYNTAX</span></span>

### <span data-ttu-id="b9420-105">GetByResourceNameNoExpandParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9420-105">GetByResourceNameNoExpandParameterSet (Default)</span></span>
```
Get-AzNetworkProfile [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9420-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9420-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9420-107">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9420-107">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9420-108">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9420-108">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9420-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9420-109">DESCRIPTION</span></span>
<span data-ttu-id="b9420-110">A **Get-AzNetworkProfile** parancsmag a meglévő hálózati profil legfelső szintű erőforrását kéri le.</span><span class="sxs-lookup"><span data-stu-id="b9420-110">The **Get-AzNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="b9420-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b9420-111">EXAMPLES</span></span>

### <span data-ttu-id="b9420-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b9420-112">Example 1</span></span>
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

<span data-ttu-id="b9420-113">Ezzel beolvassa a hálózati profil NP1 az erőforráscsoport rg1</span><span class="sxs-lookup"><span data-stu-id="b9420-113">This retrieves the network profile np1 in resource group rg1</span></span>

### <span data-ttu-id="b9420-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="b9420-114">Example 2</span></span>
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

<span data-ttu-id="b9420-115">Ezzel beolvassa az "NP" kezdetű hálózati profilokat</span><span class="sxs-lookup"><span data-stu-id="b9420-115">This retrieves the network profiles that start with "np"</span></span>

## <span data-ttu-id="b9420-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9420-116">PARAMETERS</span></span>

### <span data-ttu-id="b9420-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9420-117">-DefaultProfile</span></span>
<span data-ttu-id="b9420-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9420-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9420-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="b9420-119">-ExpandResource</span></span>
<span data-ttu-id="b9420-120">A kibontani kívánt erőforrás-hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="b9420-120">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="b9420-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b9420-121">-Name</span></span>
<span data-ttu-id="b9420-122">A hálózati profil neve.</span><span class="sxs-lookup"><span data-stu-id="b9420-122">The name of the network profile.</span></span>

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

### <span data-ttu-id="b9420-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9420-123">-ResourceGroupName</span></span>
<span data-ttu-id="b9420-124">A hálózati profil erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b9420-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="b9420-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9420-125">-ResourceId</span></span>
<span data-ttu-id="b9420-126">A hálózati profil Azure Resource Manager azonosítója</span><span class="sxs-lookup"><span data-stu-id="b9420-126">The Azure resource manager id of the network profile.</span></span>

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

### <span data-ttu-id="b9420-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9420-127">CommonParameters</span></span>
<span data-ttu-id="b9420-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9420-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9420-129">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b9420-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9420-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9420-130">INPUTS</span></span>

### <span data-ttu-id="b9420-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b9420-131">System.String</span></span>

## <span data-ttu-id="b9420-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9420-132">OUTPUTS</span></span>

### <span data-ttu-id="b9420-133">Microsoft. Azure. commands. Network. models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b9420-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="b9420-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9420-134">NOTES</span></span>

## <span data-ttu-id="b9420-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9420-135">RELATED LINKS</span></span>

[<span data-ttu-id="b9420-136">Új – AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b9420-136">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="b9420-137">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b9420-137">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="b9420-138">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b9420-138">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
