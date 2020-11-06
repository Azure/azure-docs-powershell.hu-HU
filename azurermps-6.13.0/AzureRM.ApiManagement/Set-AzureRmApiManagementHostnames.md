---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F9CE8705-F7B1-45AB-98BC-FC6DC023D38D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementhostnames
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
ms.openlocfilehash: 7093b51ffee3f0ad635da7a6c0b63d26e93e5f2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494213"
---
# <span data-ttu-id="2183e-101">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="2183e-101">Set-AzureRmApiManagementHostnames</span></span>

## <span data-ttu-id="2183e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2183e-102">SYNOPSIS</span></span>
<span data-ttu-id="2183e-103">Egyéni gépnév-konfigurációt állít be egy API-kezelési szolgáltatás-proxyhoz vagy-portálhoz.</span><span class="sxs-lookup"><span data-stu-id="2183e-103">Sets a custom hostname configuration for an API Management service proxy or portal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2183e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2183e-104">SYNTAX</span></span>

### <span data-ttu-id="2183e-105">SetSpecificService (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2183e-105">SetSpecificService (Default)</span></span>
```
Set-AzureRmApiManagementHostnames -ResourceGroupName <String> -Name <String>
 [-PortalHostnameConfiguration <PsApiManagementHostnameConfiguration>]
 [-ProxyHostnameConfiguration <PsApiManagementHostnameConfiguration>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2183e-106">SetFromPsApiManagementInstance</span><span class="sxs-lookup"><span data-stu-id="2183e-106">SetFromPsApiManagementInstance</span></span>
```
Set-AzureRmApiManagementHostnames -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2183e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2183e-107">DESCRIPTION</span></span>
<span data-ttu-id="2183e-108">A **set-AzureRmApiManagementHostnames** parancsmag egyéni állomásnév-konfigurációt alkalmaz egy API-kezelési szolgáltatási proxyra vagy portálra.</span><span class="sxs-lookup"><span data-stu-id="2183e-108">The **Set-AzureRmApiManagementHostnames** cmdlet applies a custom hostname configuration for an API Management service proxy or portal.</span></span>

## <span data-ttu-id="2183e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2183e-109">EXAMPLES</span></span>

### <span data-ttu-id="2183e-110">Példa 1: a proxy és a portál egyéni gépnév-konfigurációjának beállítása</span><span class="sxs-lookup"><span data-stu-id="2183e-110">Example 1: Set the custom hostname configuration for a proxy and portal</span></span>
```
PS C:\>Set-AzureRmApiManagementHostnames -Name ContosoApi -ResourceGroupName Contoso -PortalHostnameConfiguration $portalHostnameConf -ProxyHostnameConfiguration $proxyHostnameConf
```

<span data-ttu-id="2183e-111">Ez a parancs beállítja a proxy és a portál egyéni gépnév-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="2183e-111">This command sets the custom hostname configuration for proxy and portal.</span></span>

### <span data-ttu-id="2183e-112">2. példa: egyéni állomásnév beállítása proxyhoz és portálhoz</span><span class="sxs-lookup"><span data-stu-id="2183e-112">Example 2: Configure a custom hostname for a proxy and portal</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name ContosoApi -ResourceGroupName "Contoso" -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
PS C:\> Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName "Contoso" -HostnameType "Portal" -PfxPath "C:\portalcert.pfx" -PfxPassword "CertSecret"
PS C:\> $PortalHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
PS C:\> $ProxyHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "proxy.contoso.com" -CertificateThumbprint "5DD7CCF6A1E74E0987DD2873406B7264"
PS C:\> Set-AzureRmApiManagementHostnames -Name "ContosoApi" -ResourceGroupName "Contoso" -PortalHostnameConfiguration $PortalHostnameConf -ProxyHostnameConfiguration $ProxyHostnameConf
```

<span data-ttu-id="2183e-113">Ebben a példában egy egyéni állomásnév van beállítva a proxyhoz és a portálhoz.</span><span class="sxs-lookup"><span data-stu-id="2183e-113">This example configures a custom hostname for proxy and portal.</span></span>
<span data-ttu-id="2183e-114">Importálnia kell a megfelelő tanúsítványokat, majd alkalmaznia kell az egyéni állomásnevek nevet.</span><span class="sxs-lookup"><span data-stu-id="2183e-114">You need to import corresponding certificates and then apply the custom hostnames.</span></span>

## <span data-ttu-id="2183e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2183e-115">PARAMETERS</span></span>

### <span data-ttu-id="2183e-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2183e-116">-ApiManagement</span></span>
<span data-ttu-id="2183e-117">Azt a **PsApiManagement** -példányt adja meg, amelyből a parancsmag a *PortalHostnameConfiguration* és a *ProxyHostnameConfiguration* paramétereket kapja.</span><span class="sxs-lookup"><span data-stu-id="2183e-117">Specifies the **PsApiManagement** instance that this cmdlet gets the *PortalHostnameConfiguration* and *ProxyHostnameConfiguration* parameters from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: SetFromPsApiManagementInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2183e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2183e-118">-DefaultProfile</span></span>
<span data-ttu-id="2183e-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2183e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2183e-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2183e-120">-Name</span></span>
<span data-ttu-id="2183e-121">Az API-kezelési példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2183e-121">Specifies the name of the API Management instance.</span></span>

```yaml
Type: System.String
Parameter Sets: SetSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2183e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2183e-122">-PassThru</span></span>
<span data-ttu-id="2183e-123">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="2183e-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2183e-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2183e-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2183e-125">-PortalHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="2183e-125">-PortalHostnameConfiguration</span></span>
<span data-ttu-id="2183e-126">Az egyéni portál gépnév-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2183e-126">Specifies the custom portal hostname configuration.</span></span>
<span data-ttu-id="2183e-127">$Null átadása a parancsmaghoz az alapértelmezett állomásnév beállítása.</span><span class="sxs-lookup"><span data-stu-id="2183e-127">Passing $null to the cmdlet sets the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration
Parameter Sets: SetSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2183e-128">-ProxyHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="2183e-128">-ProxyHostnameConfiguration</span></span>
<span data-ttu-id="2183e-129">Az egyéni proxy gépnév-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2183e-129">Specifies the custom proxy hostname configuration.</span></span>
<span data-ttu-id="2183e-130">A tompított $null az alapértelmezett állomásnév beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="2183e-130">Passing $null sets the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration
Parameter Sets: SetSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2183e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2183e-131">-ResourceGroupName</span></span>
<span data-ttu-id="2183e-132">Annak az erőforrás-csoportnak a nevét adja meg, amely alatt az API-kezelési példány létezik.</span><span class="sxs-lookup"><span data-stu-id="2183e-132">Specifies the name of the resource group under which the API Management instance exists.</span></span>

```yaml
Type: System.String
Parameter Sets: SetSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2183e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2183e-133">CommonParameters</span></span>
<span data-ttu-id="2183e-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2183e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2183e-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2183e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2183e-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2183e-136">INPUTS</span></span>

### <span data-ttu-id="2183e-137">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="2183e-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="2183e-138">Paraméterek: ApiManagement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2183e-138">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="2183e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2183e-139">System.String</span></span>

### <span data-ttu-id="2183e-140">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="2183e-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="2183e-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2183e-141">OUTPUTS</span></span>

### <span data-ttu-id="2183e-142">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="2183e-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="2183e-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2183e-143">NOTES</span></span>

## <span data-ttu-id="2183e-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2183e-144">RELATED LINKS</span></span>

[<span data-ttu-id="2183e-145">Importálás – AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="2183e-145">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="2183e-146">Új – AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="2183e-146">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)


