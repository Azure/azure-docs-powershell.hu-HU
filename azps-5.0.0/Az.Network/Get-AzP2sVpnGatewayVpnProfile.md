---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
ms.openlocfilehash: 60937898e7e8c0532a0f0815ee44f2e9f75041c7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195093"
---
# <span data-ttu-id="664af-101">Get-AzP2sVpnGatewayVpnProfile</span><span class="sxs-lookup"><span data-stu-id="664af-101">Get-AzP2sVpnGatewayVpnProfile</span></span>

## <span data-ttu-id="664af-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="664af-102">SYNOPSIS</span></span>
<span data-ttu-id="664af-103">Létrehoz egy SAS URL-címet, amely az ügyfél számára a VPN-profil letöltéséhez szükséges, hogy a webhely-ügyfél beállításai pontra mutasson a P2SVpnGateway-ra.</span><span class="sxs-lookup"><span data-stu-id="664af-103">Generates and returns a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span>

## <span data-ttu-id="664af-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="664af-104">SYNTAX</span></span>

### <span data-ttu-id="664af-105">ByP2SVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="664af-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayVpnProfile [-Name <String>] -ResourceGroupName <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="664af-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="664af-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -InputObject <PSP2SVpnGateway> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="664af-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="664af-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -ResourceId <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="664af-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="664af-108">DESCRIPTION</span></span>
<span data-ttu-id="664af-109">A **Get-AzP2sVpnGatewayVpnProfile** parancsmag lehetővé teszi, hogy az ügyfél számára létrehozjon egy sas-URL-címet, és a VPN-profilt a ponttól a webhely ügyfélalkalmazás beállításra mutasson a P2SVpnGateway-ra való kapcsolódásra.</span><span class="sxs-lookup"><span data-stu-id="664af-109">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="664af-110">A webhely-ügyfél beállítása ebben a VPN-profilban lehetőség csak az adott P2SVpnGateway kapcsolódhat.</span><span class="sxs-lookup"><span data-stu-id="664af-110">Point to site client setup using this Vpn profile can connect to this specific P2SVpnGateway only.</span></span>

## <span data-ttu-id="664af-111">Példák</span><span class="sxs-lookup"><span data-stu-id="664af-111">EXAMPLES</span></span>

### <span data-ttu-id="664af-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="664af-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayVpnProfile -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -AuthenticationMethod EAPTLS


ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/8cf00031-37ec-4949-b74a-48f9021bf4c0/vpnprofile/2f132439-1051-44c6-9128-b704c1c48cf7/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=HmBSprVrs
             6hDY3x1HX958nimOjavnEjL2rlSuKIIW8Q%3D&st=2019-10-25T19%3A20%3A04Z&se=2019-10-25T20%3A20%3A04Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="664af-113">A **Get-AzP2sVpnGatewayVpnProfile** parancsmag lehetővé teszi, hogy az ügyfél számára létrehozjon egy sas-URL-címet, és a VPN-profilt a ponttól a webhely ügyfélalkalmazás beállításra mutasson a P2SVpnGateway-ra való kapcsolódásra.</span><span class="sxs-lookup"><span data-stu-id="664af-113">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="664af-114">A ProfileUrl azt a SAS-URL-címet jeleníti meg, ahonnan az ügyfél letölthet egy VPN-profilt a Point to Client Setup pontra.</span><span class="sxs-lookup"><span data-stu-id="664af-114">ProfileUrl shows the SAS url from where customer can download Vpn profile for point to site client setup.</span></span>

## <span data-ttu-id="664af-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="664af-115">PARAMETERS</span></span>

### <span data-ttu-id="664af-116">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="664af-116">-AuthenticationMethod</span></span>
<span data-ttu-id="664af-117">Hitelesítési módszer</span><span class="sxs-lookup"><span data-stu-id="664af-117">Authentication Method</span></span>

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

### <span data-ttu-id="664af-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="664af-118">-DefaultProfile</span></span>
<span data-ttu-id="664af-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="664af-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="664af-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="664af-120">-InputObject</span></span>
<span data-ttu-id="664af-121">A módosítani kívánt p2s VPN-átjáró objektum</span><span class="sxs-lookup"><span data-stu-id="664af-121">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="664af-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="664af-122">-Name</span></span>
<span data-ttu-id="664af-123">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="664af-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="664af-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="664af-124">-ResourceGroupName</span></span>
<span data-ttu-id="664af-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="664af-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="664af-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="664af-126">-ResourceId</span></span>
<span data-ttu-id="664af-127">A módosítani kívánt P2SVpnGateway Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="664af-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="664af-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="664af-128">CommonParameters</span></span>
<span data-ttu-id="664af-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="664af-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="664af-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="664af-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="664af-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="664af-131">INPUTS</span></span>

### <span data-ttu-id="664af-132">System. String</span><span class="sxs-lookup"><span data-stu-id="664af-132">System.String</span></span>
<span data-ttu-id="664af-133">Microsoft. Azure. commands. Network. models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="664af-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="664af-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="664af-134">OUTPUTS</span></span>

### <span data-ttu-id="664af-135">Microsoft. Azure. commands. Network. models. PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="664af-135">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="664af-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="664af-136">NOTES</span></span>

## <span data-ttu-id="664af-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="664af-137">RELATED LINKS</span></span>