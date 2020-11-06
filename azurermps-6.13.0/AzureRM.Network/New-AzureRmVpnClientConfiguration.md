---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientConfiguration.md
ms.openlocfilehash: ddd620bb1878106801d6c69c086dc9642e76e1c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500179"
---
# <span data-ttu-id="aff53-101">New-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="aff53-101">New-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="aff53-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aff53-102">SYNOPSIS</span></span>
<span data-ttu-id="aff53-103">Ez a parancs lehetővé teszi a felhasználóknak, hogy az előre konfigurált virtuális magánhálózati beállításokon alapuló VPN-profilokat hozzanak létre a VPN-átjárón, a további beállítások mellett, amelyeket a felhasználóknak esetleg be kell állítaniuk (például néhány főtanúsítvány esetén).</span><span class="sxs-lookup"><span data-stu-id="aff53-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aff53-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aff53-104">SYNTAX</span></span>

```
New-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-ProcessorArchitecture <String>] -AuthenticationMethod <String> [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aff53-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aff53-105">DESCRIPTION</span></span>
<span data-ttu-id="aff53-106">Ez a beállítás lehetővé teszi a felhasználóknak, hogy az előre konfigurált virtuális magánhálózati beállítások alapján hozzanak létre VPN-profilt a VPN-átjárón, a további beállítások mellett, amelyeket a felhasználóknak konfigurálniuk kell (például néhány főtanúsítvány esetén).</span><span class="sxs-lookup"><span data-stu-id="aff53-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="aff53-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aff53-107">EXAMPLES</span></span>

### <span data-ttu-id="aff53-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aff53-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="aff53-109">Ez a parancsmag a "ContosoVirtualNetworkGateway" ResourceGroup "ContosoResourceGroup" című "virtuális magánhálózati ügyfél-profil" zip-fájl létrehozásához használható.</span><span class="sxs-lookup"><span data-stu-id="aff53-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="aff53-110">A profil olyan előre konfigurált RADIUS-kiszolgálóhoz jön létre, amely a "EAPTLS" hitelesítési módszert használja az VpnProfileRadiusCert-ös tanúsítvány fájllal.</span><span class="sxs-lookup"><span data-stu-id="aff53-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="aff53-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aff53-111">PARAMETERS</span></span>

### <span data-ttu-id="aff53-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="aff53-112">-AuthenticationMethod</span></span>
<span data-ttu-id="aff53-113">A hitelesítési módszer EAPMSCHAPv2 vagy EAPTLS végezhet értékeket.</span><span class="sxs-lookup"><span data-stu-id="aff53-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="aff53-114">Ha a EAPMSCHAPv2 meg van adva, a parancsmag létrehoz egy ügyfél-konfigurációs telepítőt a Felhasználónév/jelszó hitelesítéshez, amely EAP-MSCHAPv2 hitelesítési protokollt használ.</span><span class="sxs-lookup"><span data-stu-id="aff53-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="aff53-115">Ha a EAPTLS meg van adva, a parancsmag létrehoz egy ügyfél-konfigurációs telepítőt az EAP-TLS protokollt használó tanúsítvány-hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="aff53-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="aff53-116">A "EapTls" beállítás a megbízható gyökér feltöltésével a virtuális hálózati átjáró által végzett RADIUS-alapú tanúsítvány-hitelesítés és tanúsítvány-hitelesítéshez is használható.</span><span class="sxs-lookup"><span data-stu-id="aff53-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="aff53-117">A parancsmag automatikusan észleli, hogy mi van beállítva.</span><span class="sxs-lookup"><span data-stu-id="aff53-117">The cmdlet automatically detects what is configured.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aff53-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="aff53-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="aff53-119">Az ügyféloldali főtanúsítvány elérési útjának listája</span><span class="sxs-lookup"><span data-stu-id="aff53-119">A list of client root certificate paths</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aff53-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aff53-120">-DefaultProfile</span></span>
<span data-ttu-id="aff53-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aff53-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff53-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aff53-122">-Name</span></span>
<span data-ttu-id="aff53-123">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="aff53-123">The resource name.</span></span>

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

### <span data-ttu-id="aff53-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="aff53-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="aff53-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="aff53-125">ProcessorArchitecture</span></span>

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

### <span data-ttu-id="aff53-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="aff53-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="aff53-127">A RADIUS-kiszolgáló fő tanúsítványának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="aff53-127">Radius server root certificate path.</span></span> <span data-ttu-id="aff53-128">Ez egy kötelező paraméter, amelyet meg kell adni, ha az EAP-TLS-t RADIUS-hitelesítéssel használja.</span><span class="sxs-lookup"><span data-stu-id="aff53-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="aff53-129">Ez a teljes elérési út annak a RADIUS-főtanúsítványnak a neve, amely az ügyfél által a RADIUS-kiszolgáló ellenőrzéséhez a hitelesítés során érvényes.</span><span class="sxs-lookup"><span data-stu-id="aff53-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

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

### <span data-ttu-id="aff53-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aff53-130">-ResourceGroupName</span></span>
<span data-ttu-id="aff53-131">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="aff53-131">The resource group name.</span></span>

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

### <span data-ttu-id="aff53-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aff53-132">-Confirm</span></span>
<span data-ttu-id="aff53-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aff53-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aff53-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aff53-134">-WhatIf</span></span>
<span data-ttu-id="aff53-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aff53-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aff53-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aff53-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aff53-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aff53-137">CommonParameters</span></span>
<span data-ttu-id="aff53-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aff53-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aff53-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aff53-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aff53-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aff53-140">INPUTS</span></span>

### <span data-ttu-id="aff53-141">System. String</span><span class="sxs-lookup"><span data-stu-id="aff53-141">System.String</span></span>

### <span data-ttu-id="aff53-142">System. Collections. Generic. list ' 1 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="aff53-142">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="aff53-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aff53-143">OUTPUTS</span></span>

### <span data-ttu-id="aff53-144">Microsoft. Azure. commands. Network. models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="aff53-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="aff53-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aff53-145">NOTES</span></span>

## <span data-ttu-id="aff53-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aff53-146">RELATED LINKS</span></span>
