---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 13c74416591318bdebdc869475930111e695d3f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370998"
---
# <span data-ttu-id="b3c22-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="b3c22-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="b3c22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3c22-102">SYNOPSIS</span></span>
<span data-ttu-id="b3c22-103">A P2SVpnGatewaytől a webhelykapcsolatok aktuális pontjának részletes adatait kapja.</span><span class="sxs-lookup"><span data-stu-id="b3c22-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="b3c22-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b3c22-104">SYNTAX</span></span>

### <span data-ttu-id="b3c22-105">ByP2SVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b3c22-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3c22-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="b3c22-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3c22-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="b3c22-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3c22-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b3c22-108">DESCRIPTION</span></span>
<span data-ttu-id="b3c22-109">A **Get-AzP2sVpnGatewayDetailedConnectionHealth** parancsmag lehetővé teszi a P2SVpnGatewayből a webhelykapcsolatok aktuális pontjának részletes adatait.</span><span class="sxs-lookup"><span data-stu-id="b3c22-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="b3c22-110">Az ügyfélnek át kell adnia az SAS URL-címét, ahol meg tudjuk adni ezt a részletes egészségügyi információt.</span><span class="sxs-lookup"><span data-stu-id="b3c22-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="b3c22-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b3c22-111">EXAMPLES</span></span>

### <span data-ttu-id="b3c22-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="b3c22-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="b3c22-113">A **Get-AzP2sVpnGatewayDetailedConnectionHealth** parancsmag lehetővé teszi a P2SVpnGatewayből a webhelykapcsolatok aktuális pontjának részletes adatait.</span><span class="sxs-lookup"><span data-stu-id="b3c22-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="b3c22-114">Az ügyfél letöltheti az állapotadatokat a átadott SAS URL-címről.</span><span class="sxs-lookup"><span data-stu-id="b3c22-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="b3c22-115">Itt a webhely-kapcsolat minden pontjának adatait meg fogja jelenni felhasználónévvel, bájttal, bájttal, kiosztott IP-címmel stb.</span><span class="sxs-lookup"><span data-stu-id="b3c22-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="b3c22-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3c22-116">PARAMETERS</span></span>

### <span data-ttu-id="b3c22-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3c22-117">-DefaultProfile</span></span>
<span data-ttu-id="b3c22-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b3c22-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3c22-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3c22-119">-InputObject</span></span>
<span data-ttu-id="b3c22-120">A módosítható p2s vpn átjáróobjektum</span><span class="sxs-lookup"><span data-stu-id="b3c22-120">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="b3c22-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b3c22-121">-Name</span></span>
<span data-ttu-id="b3c22-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b3c22-122">The resource name.</span></span>

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

### <span data-ttu-id="b3c22-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="b3c22-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="b3c22-124">OutputBlob Sas URL-cím, amelyre a p2s vpn kapcsolat állapota lesz megírva.</span><span class="sxs-lookup"><span data-stu-id="b3c22-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

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

### <span data-ttu-id="b3c22-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3c22-125">-ResourceGroupName</span></span>
<span data-ttu-id="b3c22-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b3c22-126">The resource group name.</span></span>

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

### <span data-ttu-id="b3c22-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3c22-127">-ResourceId</span></span>
<span data-ttu-id="b3c22-128">A módosítható P2SVpnGateway Azure-erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="b3c22-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="b3c22-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="b3c22-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="b3c22-130">A szűrni megfelelő P2S vpn-felhasználónevek listája.</span><span class="sxs-lookup"><span data-stu-id="b3c22-130">The list of P2S vpn user names to filter.</span></span>

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

### <span data-ttu-id="b3c22-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3c22-131">CommonParameters</span></span>
<span data-ttu-id="b3c22-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3c22-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3c22-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3c22-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3c22-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3c22-134">INPUTS</span></span>

### <span data-ttu-id="b3c22-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b3c22-135">System.String</span></span>
<span data-ttu-id="b3c22-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b3c22-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="b3c22-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3c22-137">OUTPUTS</span></span>

### <span data-ttu-id="b3c22-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="b3c22-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="b3c22-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b3c22-139">NOTES</span></span>

## <span data-ttu-id="b3c22-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3c22-140">RELATED LINKS</span></span>
