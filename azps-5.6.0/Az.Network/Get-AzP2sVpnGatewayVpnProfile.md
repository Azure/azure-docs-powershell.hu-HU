---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azp2svpngatewayvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
ms.openlocfilehash: e606f961cf54eb390e76e3f9bc8c00e556aff7fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919737"
---
# <span data-ttu-id="843ce-101">Get-AzP2sVpnGatewayVpnProfile</span><span class="sxs-lookup"><span data-stu-id="843ce-101">Get-AzP2sVpnGatewayVpnProfile</span></span>

## <span data-ttu-id="843ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="843ce-102">SYNOPSIS</span></span>
<span data-ttu-id="843ce-103">EGY SAS-URL-címet hoz létre és ad vissza, amely alapján az ügyfél letölti a Vpn-profilt, hogy a P2SVpnGateway-re mutató webhelykapcsolattal rendelkező ügyfélprogram-beállításra mutasson.</span><span class="sxs-lookup"><span data-stu-id="843ce-103">Generates and returns a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span>

## <span data-ttu-id="843ce-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="843ce-104">SYNTAX</span></span>

### <span data-ttu-id="843ce-105">ByP2SVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="843ce-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayVpnProfile [-Name <String>] -ResourceGroupName <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="843ce-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="843ce-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -InputObject <PSP2SVpnGateway> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="843ce-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="843ce-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -ResourceId <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="843ce-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="843ce-108">DESCRIPTION</span></span>
<span data-ttu-id="843ce-109">A **Get-AzP2sVpnGatewayVpnProfile** parancsmag lehetővé teszi, hogy EGY SAS-url-t hozzon létre és töltsön le az ügyfélnek a Vpn-profil letöltéséhez, hogy a P2SVpnGatewayre mutató webhelykapcsolatot biztosítson a webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="843ce-109">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="843ce-110">Ezzel a Vpn-profillal mutasson a webhely ügyfelének beállítására, és csak ehhez a P2SVpnGatewayhez tud csatlakozni.</span><span class="sxs-lookup"><span data-stu-id="843ce-110">Point to site client setup using this Vpn profile can connect to this specific P2SVpnGateway only.</span></span>

## <span data-ttu-id="843ce-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="843ce-111">EXAMPLES</span></span>

### <span data-ttu-id="843ce-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="843ce-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayVpnProfile -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -AuthenticationMethod EAPTLS


ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/8cf00031-37ec-4949-b74a-48f9021bf4c0/vpnprofile/2f132439-1051-44c6-9128-b704c1c48cf7/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=HmBSprVrs
             6hDY3x1HX958nimOjavnEjL2rlSuKIIW8Q%3D&st=2019-10-25T19%3A20%3A04Z&se=2019-10-25T20%3A20%3A04Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="843ce-113">A **Get-AzP2sVpnGatewayVpnProfile** parancsmag lehetővé teszi, hogy EGY SAS-url-t hozzon létre és töltsön le az ügyfélnek a Vpn-profil letöltéséhez, hogy a P2SVpnGatewayre mutató webhelykapcsolatot biztosítson a webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="843ce-113">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="843ce-114">A ProfileUrl azt az SAS URL-címet jeleníti meg, ahonnan az ügyfél letöltheti a Vpn-profilt a webhely ügyfelének beállításához.</span><span class="sxs-lookup"><span data-stu-id="843ce-114">ProfileUrl shows the SAS url from where customer can download Vpn profile for point to site client setup.</span></span>

## <span data-ttu-id="843ce-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="843ce-115">PARAMETERS</span></span>

### <span data-ttu-id="843ce-116">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="843ce-116">-AuthenticationMethod</span></span>
<span data-ttu-id="843ce-117">Hitelesítési módszer</span><span class="sxs-lookup"><span data-stu-id="843ce-117">Authentication Method</span></span>

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

### <span data-ttu-id="843ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="843ce-118">-DefaultProfile</span></span>
<span data-ttu-id="843ce-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="843ce-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="843ce-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="843ce-120">-InputObject</span></span>
<span data-ttu-id="843ce-121">A módosítható p2s vpn átjáróobjektum</span><span class="sxs-lookup"><span data-stu-id="843ce-121">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="843ce-122">-Name</span><span class="sxs-lookup"><span data-stu-id="843ce-122">-Name</span></span>
<span data-ttu-id="843ce-123">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="843ce-123">The resource name.</span></span>

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

### <span data-ttu-id="843ce-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="843ce-124">-ResourceGroupName</span></span>
<span data-ttu-id="843ce-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="843ce-125">The resource group name.</span></span>

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

### <span data-ttu-id="843ce-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="843ce-126">-ResourceId</span></span>
<span data-ttu-id="843ce-127">A módosítható P2SVpnGateway Azure-erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="843ce-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="843ce-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="843ce-128">CommonParameters</span></span>
<span data-ttu-id="843ce-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="843ce-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="843ce-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="843ce-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="843ce-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="843ce-131">INPUTS</span></span>

### <span data-ttu-id="843ce-132">System.String</span><span class="sxs-lookup"><span data-stu-id="843ce-132">System.String</span></span>
<span data-ttu-id="843ce-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="843ce-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="843ce-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="843ce-134">OUTPUTS</span></span>

### <span data-ttu-id="843ce-135">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="843ce-135">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="843ce-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="843ce-136">NOTES</span></span>

## <span data-ttu-id="843ce-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="843ce-137">RELATED LINKS</span></span>
