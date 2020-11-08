---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 13c74416591318bdebdc869475930111e695d3f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181061"
---
# <span data-ttu-id="41961-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="41961-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="41961-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41961-102">SYNOPSIS</span></span>
<span data-ttu-id="41961-103">Megtudhatja, hogy milyen részletes információk jelennek meg a P2SVpnGateway-ról a webhelyek közötti kapcsolatokról.</span><span class="sxs-lookup"><span data-stu-id="41961-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="41961-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41961-104">SYNTAX</span></span>

### <span data-ttu-id="41961-105">ByP2SVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="41961-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="41961-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="41961-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41961-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="41961-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41961-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="41961-108">DESCRIPTION</span></span>
<span data-ttu-id="41961-109">A **Get-AzP2sVpnGatewayDetailedConnectionHealth** parancsmaggal megtudhatja, hogy miként érheti el a P2SVpnGateway-ról a jelenlegi pontról származó kapcsolatok részletes információit.</span><span class="sxs-lookup"><span data-stu-id="41961-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="41961-110">Az ügyfélnek továbbítania kell a SAS URL-címét, ahol megadhatja ezeket a részletes egészségvédelmi információkat.</span><span class="sxs-lookup"><span data-stu-id="41961-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="41961-111">Példák</span><span class="sxs-lookup"><span data-stu-id="41961-111">EXAMPLES</span></span>

### <span data-ttu-id="41961-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="41961-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="41961-113">A **Get-AzP2sVpnGatewayDetailedConnectionHealth** parancsmaggal megtudhatja, hogy miként érheti el a P2SVpnGateway-ról a jelenlegi pontról származó kapcsolatok részletes információit.</span><span class="sxs-lookup"><span data-stu-id="41961-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="41961-114">Az ügyfél le tudja tölteni az állapot adatait a beérkezett SAS URL-címéről.</span><span class="sxs-lookup"><span data-stu-id="41961-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="41961-115">Ez minden pontról információt jelenít meg a webhelyekkel való kapcsolatról a felhasználónévekkel, bájtokkal, bájtokkal, kiosztott IP-címmel stb.</span><span class="sxs-lookup"><span data-stu-id="41961-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="41961-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41961-116">PARAMETERS</span></span>

### <span data-ttu-id="41961-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41961-117">-DefaultProfile</span></span>
<span data-ttu-id="41961-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41961-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41961-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41961-119">-InputObject</span></span>
<span data-ttu-id="41961-120">A módosítani kívánt p2s VPN-átjáró objektum</span><span class="sxs-lookup"><span data-stu-id="41961-120">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="41961-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="41961-121">-Name</span></span>
<span data-ttu-id="41961-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="41961-122">The resource name.</span></span>

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

### <span data-ttu-id="41961-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="41961-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="41961-124">A OutputBlob sas URL-címe, amelyhez a p2s VPN-kapcsolat állapota lesz írva.</span><span class="sxs-lookup"><span data-stu-id="41961-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41961-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41961-125">-ResourceGroupName</span></span>
<span data-ttu-id="41961-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="41961-126">The resource group name.</span></span>

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

### <span data-ttu-id="41961-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41961-127">-ResourceId</span></span>
<span data-ttu-id="41961-128">A módosítani kívánt P2SVpnGateway Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="41961-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="41961-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="41961-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="41961-130">A P2S VPN-Felhasználónevek listája a szűréshez.</span><span class="sxs-lookup"><span data-stu-id="41961-130">The list of P2S vpn user names to filter.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41961-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41961-131">CommonParameters</span></span>
<span data-ttu-id="41961-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41961-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41961-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41961-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41961-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41961-134">INPUTS</span></span>

### <span data-ttu-id="41961-135">System. String</span><span class="sxs-lookup"><span data-stu-id="41961-135">System.String</span></span>
<span data-ttu-id="41961-136">Microsoft. Azure. commands. Network. models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="41961-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="41961-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41961-137">OUTPUTS</span></span>

### <span data-ttu-id="41961-138">Microsoft. Azure. commands. Network. models. PSP2SVpnConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="41961-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="41961-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41961-139">NOTES</span></span>

## <span data-ttu-id="41961-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41961-140">RELATED LINKS</span></span>
