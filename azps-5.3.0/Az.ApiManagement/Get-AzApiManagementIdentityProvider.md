---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: b267fc854127c1cb098481ac483a7572c8b2e12f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478957"
---
# <span data-ttu-id="f2151-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f2151-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="f2151-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2151-102">SYNOPSIS</span></span>
<span data-ttu-id="f2151-103">Az identitásszolgáltató konfigurációjának részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="f2151-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="f2151-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f2151-104">SYNTAX</span></span>

### <span data-ttu-id="f2151-105">AllIdentityProviders (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f2151-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2151-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="f2151-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2151-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f2151-107">DESCRIPTION</span></span>
<span data-ttu-id="f2151-108">Az identitásszolgáltató konfigurációjának részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="f2151-108">Get the identity provider configuration details.</span></span>
<span data-ttu-id="f2151-109">A ClientSecret nem fog szerepelni az eredmény részletei között.</span><span class="sxs-lookup"><span data-stu-id="f2151-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="f2151-110">Az ügyfél titkosságát a **Get-AzApiManagementIdentityProviderClientSecret használatával használhatja.**</span><span class="sxs-lookup"><span data-stu-id="f2151-110">To get client secret, use **Get-AzApiManagementIdentityProviderClientSecret**.</span></span>

## <span data-ttu-id="f2151-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f2151-111">EXAMPLES</span></span>

### <span data-ttu-id="f2151-112">1. példa: Az összes identitásszolgáltató lekérte</span><span class="sxs-lookup"><span data-stu-id="f2151-112">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="f2151-113">Szerezze be a szolgáltatás összes konfigurációszolgáltatóját.</span><span class="sxs-lookup"><span data-stu-id="f2151-113">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="f2151-114">2. példa: Az AAD-típus identitásszolgáltatójának lekérte</span><span class="sxs-lookup"><span data-stu-id="f2151-114">Example 2: Get the AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $apimContext -Type Aad


Type                     : Aad
ClientId                 : aaa
ClientSecret             : xxxxx
AllowedTenants           : {contosotest.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         :
SigninPolicyName         :
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             :
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/Aad
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="f2151-115">Az Azure Active Directory identitásszolgáltató-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f2151-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="f2151-116">3. példa: Az AAD B2C típusú identitásszolgáltató lekérte</span><span class="sxs-lookup"><span data-stu-id="f2151-116">Example 3: Get the AAD B2C Type Identity Provider</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $context -Type AadB2C


Type                     : AadB2C
ClientId                 : f02dafe2-b8b8-48ec-a38e-27e5c16c51e5
ClientSecret             : xxxxxx
AllowedTenants           : {contosoaadb2c.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         : B2C_1_policy-signup
SigninPolicyName         : B2C_1_policy-signin
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             : contosoaadb2c.onmicrosoft.com
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/AadB2C
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="f2151-117">Az Azure Active Directory identitásszolgáltató-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f2151-117">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="f2151-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2151-118">PARAMETERS</span></span>

### <span data-ttu-id="f2151-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f2151-119">-Context</span></span>
<span data-ttu-id="f2151-120">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="f2151-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f2151-121">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="f2151-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2151-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2151-122">-DefaultProfile</span></span>
<span data-ttu-id="f2151-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2151-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2151-124">-Type</span><span class="sxs-lookup"><span data-stu-id="f2151-124">-Type</span></span>
<span data-ttu-id="f2151-125">Identitásszolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f2151-125">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="f2151-126">Ha meg van adva, a rendszer megpróbálja megtalálni az identitásszolgáltató konfigurációját az azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="f2151-126">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="f2151-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="f2151-127">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2151-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2151-128">CommonParameters</span></span>
<span data-ttu-id="f2151-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2151-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2151-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2151-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2151-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2151-131">INPUTS</span></span>

### <span data-ttu-id="f2151-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f2151-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f2151-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="f2151-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="f2151-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2151-134">OUTPUTS</span></span>

### <span data-ttu-id="f2151-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f2151-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="f2151-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f2151-136">NOTES</span></span>

## <span data-ttu-id="f2151-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2151-137">RELATED LINKS</span></span>
