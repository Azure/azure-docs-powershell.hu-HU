---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfigurationvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
ms.openlocfilehash: 5e19f63c0497535c44513c55a28d7117d0783574
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195563"
---
# <span data-ttu-id="d449a-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span><span class="sxs-lookup"><span data-stu-id="d449a-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span></span>

## <span data-ttu-id="d449a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d449a-102">SYNOPSIS</span></span>
<span data-ttu-id="d449a-103">Virtuális magánhálózati profilt hoz létre és tölt le VirtualWan-VpnServerConfiguration szinten a webhely ügyfélalkalmazás beállításai pontra.</span><span class="sxs-lookup"><span data-stu-id="d449a-103">Generates and downloads Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="d449a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d449a-104">SYNTAX</span></span>

### <span data-ttu-id="d449a-105">ByVirtualWanNameByVpnServerConfigurationObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d449a-105">ByVirtualWanNameByVpnServerConfigurationObject (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d449a-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="d449a-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d449a-107">ByVirtualWanObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="d449a-107">ByVirtualWanObjectByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d449a-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="d449a-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d449a-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="d449a-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d449a-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="d449a-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String> -VpnServerConfigurationId <String>
 [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d449a-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="d449a-111">DESCRIPTION</span></span>
<span data-ttu-id="d449a-112">A **Get-AzVirtualWanVpnServerConfigurationVpnProfile** parancsmag lehetővé teszi a VPN-profil generálását és letöltését VirtualWan-VpnServerConfiguration szinten a webhely ügyfélalkalmazás beállításához.</span><span class="sxs-lookup"><span data-stu-id="d449a-112">The **Get-AzVirtualWanVpnServerConfigurationVpnProfile** cmdlet enables you to generate and download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span> <span data-ttu-id="d449a-113">Erre a pontról a webhelyről az Azure P2SVpnGateway-ra való kapcsolódási pontra van szükség.</span><span class="sxs-lookup"><span data-stu-id="d449a-113">This is required for Point to site connectivity from Point to site client to Azure P2SVpnGateway.</span></span>

## <span data-ttu-id="d449a-114">Példák</span><span class="sxs-lookup"><span data-stu-id="d449a-114">EXAMPLES</span></span>

### <span data-ttu-id="d449a-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d449a-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfigurationVpnProfile -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting -VpnServerConfiguration $vpnServerConfig -AuthenticationMethod EAPTLS

ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/aa316f33-d0f6-4e61-994a-9aa24c0e5f70/vpnprofile/eb99aa3d-1106-49eb-9644-791c045c5cca/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=kZinevNqW
             qsEAbWAcYiKfUHFxZzh2hwvtb49dfVtUDA%3D&st=2019-10-25T19%3A52%3A36Z&se=2019-10-25T20%3A52%3A36Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="d449a-116">A fenti parancs generálja és visszaállítja a SAS URL-t az ügyfélnek a VPN-profil letöltéséhez VirtualWan-VpnServerConfiguration szinten a webhely ügyfélalkalmazás beállításához.</span><span class="sxs-lookup"><span data-stu-id="d449a-116">The above command will generate and returns SAS Url for customer to download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="d449a-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d449a-117">PARAMETERS</span></span>

### <span data-ttu-id="d449a-118">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="d449a-118">-AuthenticationMethod</span></span>
<span data-ttu-id="d449a-119">Hitelesítési módszer</span><span class="sxs-lookup"><span data-stu-id="d449a-119">Authentication Method</span></span>

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

### <span data-ttu-id="d449a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d449a-120">-DefaultProfile</span></span>
<span data-ttu-id="d449a-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d449a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d449a-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d449a-122">-Name</span></span>
<span data-ttu-id="d449a-123">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d449a-123">The resource name.</span></span>

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

### <span data-ttu-id="d449a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d449a-124">-ResourceGroupName</span></span>
<span data-ttu-id="d449a-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="d449a-125">The resource group name.</span></span>

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

### <span data-ttu-id="d449a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d449a-126">-ResourceId</span></span>
<span data-ttu-id="d449a-127">A virtuális WAN Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="d449a-127">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="d449a-128">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="d449a-128">-VirtualWanObject</span></span>
<span data-ttu-id="d449a-129">A virtuális WAN-objektum.</span><span class="sxs-lookup"><span data-stu-id="d449a-129">The virtual wan object.</span></span>

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

### <span data-ttu-id="d449a-130">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d449a-130">-VpnServerConfiguration</span></span>
<span data-ttu-id="d449a-131">Az a VpnServerConfiguration, amelyhez ez a VirtualWan társítva van.</span><span class="sxs-lookup"><span data-stu-id="d449a-131">The VpnServerConfiguration with which this VirtualWan is associated.</span></span>

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

### <span data-ttu-id="d449a-132">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d449a-132">-VpnServerConfigurationId</span></span>
<span data-ttu-id="d449a-133">A VPN-kiszolgáló configuraiton objektum azonosítója: ezt a virtuális WAN-kapcsolattal társítja a program.</span><span class="sxs-lookup"><span data-stu-id="d449a-133">The id of Vpn server configuraiton object this Virtual wan will be associated with.</span></span>

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

### <span data-ttu-id="d449a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d449a-134">CommonParameters</span></span>
<span data-ttu-id="d449a-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d449a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d449a-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d449a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d449a-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d449a-137">INPUTS</span></span>

### <span data-ttu-id="d449a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d449a-138">System.String</span></span>
<span data-ttu-id="d449a-139">Microsoft. Azure. commands. Network. models. PSVirtualWan Microsoft. Azure. Command. Network. models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d449a-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="d449a-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d449a-140">OUTPUTS</span></span>

### <span data-ttu-id="d449a-141">Microsoft. Azure. commands. Network. models. PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="d449a-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="d449a-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d449a-142">NOTES</span></span>

## <span data-ttu-id="d449a-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d449a-143">RELATED LINKS</span></span>
