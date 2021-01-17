---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: a5c619a88f9366699f37124eab5afb2302717762
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478818"
---
# <span data-ttu-id="59f67-101">New-AzApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="59f67-101">New-AzApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="59f67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59f67-102">SYNOPSIS</span></span>
<span data-ttu-id="59f67-103">Létrehozza a `PsApiManagementCustomHostNameConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="59f67-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

## <span data-ttu-id="59f67-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="59f67-104">SYNTAX</span></span>

### <span data-ttu-id="59f67-105">NoChangeCertificate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="59f67-105">NoChangeCertificate (Default)</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59f67-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="59f67-106">SslCertificateFromFile</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -PfxPath <String> [-PfxPassword <SecureString>] [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59f67-107">SslCertificateFromKeyVault</span><span class="sxs-lookup"><span data-stu-id="59f67-107">SslCertificateFromKeyVault</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -KeyVaultId <String> [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59f67-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="59f67-108">DESCRIPTION</span></span>
<span data-ttu-id="59f67-109">A **New-AzApiManagementCustomHostnameConfiguration** parancsmag egy segítő parancs, amely létrehozza a **PsApiManagementCustomHostNameConfiguration** példányt.</span><span class="sxs-lookup"><span data-stu-id="59f67-109">The **New-AzApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="59f67-110">Ezt a parancsot a parancsmaggal együtt New-AzApiManagement és Set-AzApiManagement is.</span><span class="sxs-lookup"><span data-stu-id="59f67-110">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="59f67-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="59f67-111">EXAMPLES</span></span>

### <span data-ttu-id="59f67-112">1. példa: PsApiManagementCustomHostNameConfiguration példány létrehozása és inicializálása egy ssl tanúsítvány használatával fájlból</span><span class="sxs-lookup"><span data-stu-id="59f67-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="59f67-113">Ez a parancs létrehozza és inicializálja a **PsApiManagementCustomHostNameConfiguration** for Portal példányt.</span><span class="sxs-lookup"><span data-stu-id="59f67-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="59f67-114">Ezután létrehoz egy új ApiManagement szolgáltatást egyéni állomásnév-konfigurációval.</span><span class="sxs-lookup"><span data-stu-id="59f67-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="59f67-115">2. példa: A PsApiManagementCustomHostNameConfiguration példány létrehozása és inicializálása KeyVault-erőforrásból származó titkos mező használatával</span><span class="sxs-lookup"><span data-stu-id="59f67-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -SystemAssignedIdentity
```

<span data-ttu-id="59f67-116">Ez a parancs létrehozza és inicializálja a **PsApiManagementCustomHostNameConfiguration példányt.**</span><span class="sxs-lookup"><span data-stu-id="59f67-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="59f67-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59f67-117">PARAMETERS</span></span>

### <span data-ttu-id="59f67-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59f67-118">-DefaultProfile</span></span>
<span data-ttu-id="59f67-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59f67-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59f67-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="59f67-120">-DefaultSslBinding</span></span>
<span data-ttu-id="59f67-121">Meghatározza, hogy az érték titkos-e, és titkosítva kell-e lennie.</span><span class="sxs-lookup"><span data-stu-id="59f67-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="59f67-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="59f67-122">This parameter is optional.</span></span>
<span data-ttu-id="59f67-123">Az alapértelmezett érték hamis.</span><span class="sxs-lookup"><span data-stu-id="59f67-123">Default Value is false.</span></span>

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

### <span data-ttu-id="59f67-124">-Hostname</span><span class="sxs-lookup"><span data-stu-id="59f67-124">-Hostname</span></span>
<span data-ttu-id="59f67-125">Custom Hostname</span><span class="sxs-lookup"><span data-stu-id="59f67-125">Custom Hostname</span></span>

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

### <span data-ttu-id="59f67-126">-HostNameCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="59f67-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="59f67-127">Meglévő tanúsítványkonfiguráció.</span><span class="sxs-lookup"><span data-stu-id="59f67-127">Existing Certificate Configuration.</span></span>

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

### <span data-ttu-id="59f67-128">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="59f67-128">-HostnameType</span></span>
<span data-ttu-id="59f67-129">Állomásnév típusa</span><span class="sxs-lookup"><span data-stu-id="59f67-129">Hostname Type</span></span>

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

### <span data-ttu-id="59f67-130">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="59f67-130">-KeyVaultId</span></span>
<span data-ttu-id="59f67-131">KeyVaultId az egyéni SSL-tanúsítvány titkos tárolására.</span><span class="sxs-lookup"><span data-stu-id="59f67-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

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

### <span data-ttu-id="59f67-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="59f67-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="59f67-133">Meghatározza, hogy az érték titkos-e, és titkosítva kell-e lennie.</span><span class="sxs-lookup"><span data-stu-id="59f67-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="59f67-134">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="59f67-134">This parameter is optional.</span></span>
<span data-ttu-id="59f67-135">Az alapértelmezett érték hamis.</span><span class="sxs-lookup"><span data-stu-id="59f67-135">Default Value is false.</span></span>

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

### <span data-ttu-id="59f67-136">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="59f67-136">-PfxPassword</span></span>
<span data-ttu-id="59f67-137">A .pfx tanúsítványfájl jelszava.</span><span class="sxs-lookup"><span data-stu-id="59f67-137">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="59f67-138">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="59f67-138">-PfxPath</span></span>
<span data-ttu-id="59f67-139">A .pfx tanúsítványfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="59f67-139">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="59f67-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59f67-140">CommonParameters</span></span>
<span data-ttu-id="59f67-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59f67-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59f67-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59f67-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59f67-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59f67-143">INPUTS</span></span>

### <span data-ttu-id="59f67-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="59f67-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="59f67-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59f67-145">OUTPUTS</span></span>

### <span data-ttu-id="59f67-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span><span class="sxs-lookup"><span data-stu-id="59f67-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="59f67-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="59f67-147">NOTES</span></span>

## <span data-ttu-id="59f67-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59f67-148">RELATED LINKS</span></span>

[<span data-ttu-id="59f67-149">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="59f67-149">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="59f67-150">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="59f67-150">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)