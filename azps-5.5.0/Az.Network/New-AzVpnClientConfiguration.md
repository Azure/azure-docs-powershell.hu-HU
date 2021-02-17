---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: 11b18f0a0f12a82e88694fd91ce89956951a4eb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156866"
---
# <span data-ttu-id="d895f-101">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="d895f-101">New-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="d895f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d895f-102">SYNOPSIS</span></span>
<span data-ttu-id="d895f-103">Ezzel a paranccsal a felhasználók létrehozhatják a Vpn-profilcsomagot a VPN-átjárón előre konfigurált VPN-beállítások alapján, valamint néhány további, a felhasználók által konfigurálandó beállításon kívül (például néhány főtanúsítvány esetében).</span><span class="sxs-lookup"><span data-stu-id="d895f-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="d895f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d895f-104">SYNTAX</span></span>

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d895f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d895f-105">DESCRIPTION</span></span>
<span data-ttu-id="d895f-106">Ez lehetővé teszi a felhasználóknak, hogy a VPN-átjárón előre konfigurált VPN-beállítások alapján létrehozták a Vpn-profilcsomagot, valamint néhány további, a felhasználóknak esetleg konfigurálható beállítást is ( például néhány főtanúsítványhoz).</span><span class="sxs-lookup"><span data-stu-id="d895f-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="d895f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d895f-107">EXAMPLES</span></span>

### <span data-ttu-id="d895f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="d895f-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="d895f-109">Ez a parancsmag egy VPN-ügyfélprofil zip fájl létrehozásához használható a "ContosoVirtualNetworkGateway" számára a ResourceGroup "ContosoResourceGroup" csoportban.</span><span class="sxs-lookup"><span data-stu-id="d895f-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="d895f-110">A profil egy előre konfigurált sugárkiszolgálóhoz jön létre, amely úgy van konfigurálva, hogy az "EAPTLS" hitelesítési módszert használja a VpnProfileRadiusCert tanúsítványfájllal.</span><span class="sxs-lookup"><span data-stu-id="d895f-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="d895f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d895f-111">PARAMETERS</span></span>

### <span data-ttu-id="d895f-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="d895f-112">-AuthenticationMethod</span></span>
<span data-ttu-id="d895f-113">A hitelesítési módszer az EAPMSCHAPv2 vagy az EAPTLS értéket is veszi fel.</span><span class="sxs-lookup"><span data-stu-id="d895f-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="d895f-114">Az EAPMSCHAPv2 megadása után a parancsmag létrehoz egy ügyfélkonfigurációs telepítőt a felhasználónév/jelszó hitelesítéséhez, amely EAP-MSCHAPv2 hitelesítési protokollt használ.</span><span class="sxs-lookup"><span data-stu-id="d895f-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="d895f-115">Ha az EAPTLS meg van adva, akkor a parancsmag létrehoz egy ügyfélkonfigurációs telepítőt az EAP-TLS protokollt használó tanúsítvány-hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="d895f-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="d895f-116">Az "EapTls" lehetőség használható a VIRTUÁLIS hálózati átjáró által a megbízható legfelső szintű hitelesítés feltöltésével végzett, a SUGÁRALAPÚ tanúsítvány-hitelesítéshez és a hitelesítés-hitelesítéshez is.</span><span class="sxs-lookup"><span data-stu-id="d895f-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="d895f-117">A parancsmag automatikusan észleli a konfigurált adatokat.</span><span class="sxs-lookup"><span data-stu-id="d895f-117">The cmdlet automatically detects what is configured.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d895f-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="d895f-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="d895f-119">Az ügyfél legfelső szintű tanúsítványának elérési útjai</span><span class="sxs-lookup"><span data-stu-id="d895f-119">A list of client root certificate paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d895f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d895f-120">-DefaultProfile</span></span>
<span data-ttu-id="d895f-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d895f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d895f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d895f-122">-Name</span></span>
<span data-ttu-id="d895f-123">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d895f-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d895f-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="d895f-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="d895f-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="d895f-125">ProcessorArchitecture</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d895f-126">-RootRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="d895f-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="d895f-127">A sugárkiszolgáló gyökértanúsítványának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="d895f-127">Radius server root certificate path.</span></span> <span data-ttu-id="d895f-128">Ez egy kötelező paraméter, amely meg kell, hogy legyen adva a SUGAR-hitelesítéssel használt EAP-TLS esetén.</span><span class="sxs-lookup"><span data-stu-id="d895f-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="d895f-129">Ez annak a .cer fájlnak a teljes elérési útja, amely azt a ROOT-tanúsítványt tartalmazza, amely az ügyfél által a SUGAR-kiszolgáló hitelesítés során való érvényesítéséhez használható.</span><span class="sxs-lookup"><span data-stu-id="d895f-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d895f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d895f-130">-ResourceGroupName</span></span>
<span data-ttu-id="d895f-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d895f-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d895f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d895f-132">-Confirm</span></span>
<span data-ttu-id="d895f-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d895f-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d895f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d895f-134">-WhatIf</span></span>
<span data-ttu-id="d895f-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d895f-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d895f-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d895f-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d895f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d895f-137">CommonParameters</span></span>
<span data-ttu-id="d895f-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d895f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d895f-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d895f-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d895f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d895f-140">INPUTS</span></span>

### <span data-ttu-id="d895f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d895f-141">System.String</span></span>

### <span data-ttu-id="d895f-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d895f-142">System.String[]</span></span>

## <span data-ttu-id="d895f-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d895f-143">OUTPUTS</span></span>

### <span data-ttu-id="d895f-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="d895f-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="d895f-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d895f-145">NOTES</span></span>

## <span data-ttu-id="d895f-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d895f-146">RELATED LINKS</span></span>

[<span data-ttu-id="d895f-147">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="d895f-147">Get-AzVpnClientConfiguration</span></span>](./Get-AzVpnClientConfiguration.md)
