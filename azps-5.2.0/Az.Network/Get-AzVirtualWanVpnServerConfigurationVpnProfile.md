---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfigurationvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
ms.openlocfilehash: 5e19f63c0497535c44513c55a28d7117d0783574
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372579"
---
# <span data-ttu-id="39f34-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span><span class="sxs-lookup"><span data-stu-id="39f34-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span></span>

## <span data-ttu-id="39f34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39f34-102">SYNOPSIS</span></span>
<span data-ttu-id="39f34-103">Virtuális magánhálózati profilt hoz létre és tölt le VirtualWan-VpnServerConfiguration szinten a Point to site client beállításához.</span><span class="sxs-lookup"><span data-stu-id="39f34-103">Generates and downloads Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="39f34-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="39f34-104">SYNTAX</span></span>

### <span data-ttu-id="39f34-105">ByVirtualWanNameByVpnServerConfigurationObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39f34-105">ByVirtualWanNameByVpnServerConfigurationObject (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39f34-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="39f34-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="39f34-107">ByVirtualWanObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="39f34-107">ByVirtualWanObjectByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39f34-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="39f34-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="39f34-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="39f34-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39f34-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="39f34-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String> -VpnServerConfigurationId <String>
 [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39f34-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="39f34-111">DESCRIPTION</span></span>
<span data-ttu-id="39f34-112">A **Get-AzVirtualWanVpnServerConfigurationVpnProfile** parancsmag lehetővé teszi VirtualWan-VpnServerConfiguration Virtuális magánhálózati profil létrehozásának és letöltésének VirtualWan-VpnServerConfiguration szinten a Point to site client beállítását.</span><span class="sxs-lookup"><span data-stu-id="39f34-112">The **Get-AzVirtualWanVpnServerConfigurationVpnProfile** cmdlet enables you to generate and download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span> <span data-ttu-id="39f34-113">Ez akkor szükséges, ha a Point to site connectivity (A point to site client) és az Azure P2SVpnGateway között van szükség.</span><span class="sxs-lookup"><span data-stu-id="39f34-113">This is required for Point to site connectivity from Point to site client to Azure P2SVpnGateway.</span></span>

## <span data-ttu-id="39f34-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="39f34-114">EXAMPLES</span></span>

### <span data-ttu-id="39f34-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="39f34-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfigurationVpnProfile -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting -VpnServerConfiguration $vpnServerConfig -AuthenticationMethod EAPTLS

ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/aa316f33-d0f6-4e61-994a-9aa24c0e5f70/vpnprofile/eb99aa3d-1106-49eb-9644-791c045c5cca/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=kZinevNqW
             qsEAbWAcYiKfUHFxZzh2hwvtb49dfVtUDA%3D&st=2019-10-25T19%3A52%3A36Z&se=2019-10-25T20%3A52%3A36Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="39f34-116">A fenti parancs létrehozza és visszaadja az ÜGYFÉL URL-címét, hogy az ügyfél letöltse a Vpn-profilt VirtualWan-VpnServerConfiguration szinten a Point to site client beállításához.</span><span class="sxs-lookup"><span data-stu-id="39f34-116">The above command will generate and returns SAS Url for customer to download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="39f34-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39f34-117">PARAMETERS</span></span>

### <span data-ttu-id="39f34-118">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="39f34-118">-AuthenticationMethod</span></span>
<span data-ttu-id="39f34-119">Hitelesítési módszer</span><span class="sxs-lookup"><span data-stu-id="39f34-119">Authentication Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f34-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39f34-120">-DefaultProfile</span></span>
<span data-ttu-id="39f34-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39f34-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f34-122">-Name</span><span class="sxs-lookup"><span data-stu-id="39f34-122">-Name</span></span>
<span data-ttu-id="39f34-123">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="39f34-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f34-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39f34-124">-ResourceGroupName</span></span>
<span data-ttu-id="39f34-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="39f34-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f34-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39f34-126">-ResourceId</span></span>
<span data-ttu-id="39f34-127">A virtuális wan Azure-erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="39f34-127">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceIdByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39f34-128">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="39f34-128">-VirtualWanObject</span></span>
<span data-ttu-id="39f34-129">A virtuális wan objektum.</span><span class="sxs-lookup"><span data-stu-id="39f34-129">The virtual wan object.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39f34-130">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="39f34-130">-VpnServerConfiguration</span></span>
<span data-ttu-id="39f34-131">Az a VpnServerConfiguration, amelyhez ez a VirtualWan társítva van.</span><span class="sxs-lookup"><span data-stu-id="39f34-131">The VpnServerConfiguration with which this VirtualWan is associated.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39f34-132">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="39f34-132">-VpnServerConfigurationId</span></span>
<span data-ttu-id="39f34-133">A virtuális wanhoz társított Vpn-kiszolgáló configuraiton objektum azonosítója.</span><span class="sxs-lookup"><span data-stu-id="39f34-133">The id of Vpn server configuraiton object this Virtual wan will be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationResourceId, ByVirtualWanObjectByVpnServerConfigurationResourceId, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39f34-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39f34-134">CommonParameters</span></span>
<span data-ttu-id="39f34-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39f34-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39f34-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39f34-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39f34-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39f34-137">INPUTS</span></span>

### <span data-ttu-id="39f34-138">System.String</span><span class="sxs-lookup"><span data-stu-id="39f34-138">System.String</span></span>
<span data-ttu-id="39f34-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="39f34-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="39f34-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39f34-140">OUTPUTS</span></span>

### <span data-ttu-id="39f34-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="39f34-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="39f34-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="39f34-142">NOTES</span></span>

## <span data-ttu-id="39f34-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39f34-143">RELATED LINKS</span></span>
