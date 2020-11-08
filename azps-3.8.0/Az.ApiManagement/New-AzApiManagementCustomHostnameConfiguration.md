---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: 412bd02e43d600788fa92583a177be536e2be7ed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012245"
---
# <span data-ttu-id="643e5-101">New-AzApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="643e5-101">New-AzApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="643e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="643e5-102">SYNOPSIS</span></span>
<span data-ttu-id="643e5-103">Létrehozza a példányát `PsApiManagementCustomHostNameConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="643e5-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

## <span data-ttu-id="643e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="643e5-104">SYNTAX</span></span>

### <span data-ttu-id="643e5-105">NoChangeCertificate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="643e5-105">NoChangeCertificate (Default)</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="643e5-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="643e5-106">SslCertificateFromFile</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -PfxPath <String> [-PfxPassword <SecureString>] [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="643e5-107">SslCertificateFromKeyVault</span><span class="sxs-lookup"><span data-stu-id="643e5-107">SslCertificateFromKeyVault</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -KeyVaultId <String> [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="643e5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="643e5-108">DESCRIPTION</span></span>
<span data-ttu-id="643e5-109">A **New-AzApiManagementCustomHostnameConfiguration** parancsmag egy olyan segítő parancs, amely a **PsApiManagementCustomHostNameConfiguration** példányát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="643e5-109">The **New-AzApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="643e5-110">Ezt a parancsot a New-AzApiManagement és a Set-AzApiManagement parancsmag használja.</span><span class="sxs-lookup"><span data-stu-id="643e5-110">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="643e5-111">Példák</span><span class="sxs-lookup"><span data-stu-id="643e5-111">EXAMPLES</span></span>

### <span data-ttu-id="643e5-112">Példa 1: PsApiManagementCustomHostNameConfiguration-példány létrehozása és inicializálása SSL-tanúsítvánnyal fájlból</span><span class="sxs-lookup"><span data-stu-id="643e5-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="643e5-113">Ezzel a paranccsal létrehozhatja és inicializálhatja a **PsApiManagementCustomHostNameConfiguration** a portálra.</span><span class="sxs-lookup"><span data-stu-id="643e5-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="643e5-114">Ezután létrehoz egy új ApiManagement szolgáltatást az egyéni gépnév-konfigurációval.</span><span class="sxs-lookup"><span data-stu-id="643e5-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="643e5-115">2. példa: a PsApiManagementCustomHostNameConfiguration-példányok létrehozása és inicializálása titkos kulccsal</span><span class="sxs-lookup"><span data-stu-id="643e5-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -AssignIdentity
```

<span data-ttu-id="643e5-116">Ezzel a paranccsal létrehozhatja és inicializálhatja a **PsApiManagementCustomHostNameConfiguration** példányát.</span><span class="sxs-lookup"><span data-stu-id="643e5-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="643e5-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="643e5-117">PARAMETERS</span></span>

### <span data-ttu-id="643e5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="643e5-118">-DefaultProfile</span></span>
<span data-ttu-id="643e5-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="643e5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="643e5-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="643e5-120">-DefaultSslBinding</span></span>
<span data-ttu-id="643e5-121">Azt határozza meg, hogy az érték titkos-e, és hogy titkosított-e.</span><span class="sxs-lookup"><span data-stu-id="643e5-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="643e5-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="643e5-122">This parameter is optional.</span></span>
<span data-ttu-id="643e5-123">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="643e5-123">Default Value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="643e5-124">-Hostname (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="643e5-124">-Hostname</span></span>
<span data-ttu-id="643e5-125">Egyéni állomásnév</span><span class="sxs-lookup"><span data-stu-id="643e5-125">Custom Hostname</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="643e5-126">-HostNameCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="643e5-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="643e5-127">Létező tanúsítvány-konfiguráció</span><span class="sxs-lookup"><span data-stu-id="643e5-127">Existing Certificate Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation
Parameter Sets: NoChangeCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="643e5-128">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="643e5-128">-HostnameType</span></span>
<span data-ttu-id="643e5-129">Állomásnév típusa</span><span class="sxs-lookup"><span data-stu-id="643e5-129">Hostname Type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases:
Accepted values: Proxy, Portal, Management, Scm, DeveloperPortal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="643e5-130">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="643e5-130">-KeyVaultId</span></span>
<span data-ttu-id="643e5-131">KeyVaultId az egyéni SSL-tanúsítványt tároló titokra.</span><span class="sxs-lookup"><span data-stu-id="643e5-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="643e5-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="643e5-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="643e5-133">Azt határozza meg, hogy az érték titkos-e, és hogy titkosított-e.</span><span class="sxs-lookup"><span data-stu-id="643e5-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="643e5-134">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="643e5-134">This parameter is optional.</span></span>
<span data-ttu-id="643e5-135">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="643e5-135">Default Value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="643e5-136">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="643e5-136">-PfxPassword</span></span>
<span data-ttu-id="643e5-137">A. pfx tanúsítványfájl jelszava.</span><span class="sxs-lookup"><span data-stu-id="643e5-137">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SslCertificateFromFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="643e5-138">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="643e5-138">-PfxPath</span></span>
<span data-ttu-id="643e5-139">A. pfx tanúsítványfájl elérési útvonala.</span><span class="sxs-lookup"><span data-stu-id="643e5-139">Path to a .pfx certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="643e5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="643e5-140">CommonParameters</span></span>
<span data-ttu-id="643e5-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="643e5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="643e5-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="643e5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="643e5-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="643e5-143">INPUTS</span></span>

### <span data-ttu-id="643e5-144">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="643e5-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="643e5-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="643e5-145">OUTPUTS</span></span>

### <span data-ttu-id="643e5-146">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementCustomHostNameConfiguration</span><span class="sxs-lookup"><span data-stu-id="643e5-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="643e5-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="643e5-147">NOTES</span></span>

## <span data-ttu-id="643e5-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="643e5-148">RELATED LINKS</span></span>

[<span data-ttu-id="643e5-149">Új – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="643e5-149">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="643e5-150">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="643e5-150">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)