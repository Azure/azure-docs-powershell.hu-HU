---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 1a46cccc38e1b562786e9eda88f3336430559fc0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014374"
---
# <span data-ttu-id="b54fa-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b54fa-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="b54fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b54fa-102">SYNOPSIS</span></span>
<span data-ttu-id="b54fa-103">OpenID Connect-szolgáltatókat kap.</span><span class="sxs-lookup"><span data-stu-id="b54fa-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="b54fa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b54fa-104">SYNTAX</span></span>

### <span data-ttu-id="b54fa-105">GetAllOpenIdConnectProviders (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b54fa-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b54fa-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="b54fa-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b54fa-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="b54fa-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b54fa-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b54fa-108">DESCRIPTION</span></span>
<span data-ttu-id="b54fa-109">A **Get-AzApiManagementOpenIdConnectProvider** parancsmag openID Connect-szolgáltatókat kap az Azure API Management szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="b54fa-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>
<span data-ttu-id="b54fa-110">A ClientSecret nem fog szerepelni az eredmény részletei között.</span><span class="sxs-lookup"><span data-stu-id="b54fa-110">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="b54fa-111">Az ügyfél titkosítására használja a **Get-AzApiManagementOpenIdConnectProviderClientSecretet.**</span><span class="sxs-lookup"><span data-stu-id="b54fa-111">To get client secret, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span></span>

## <span data-ttu-id="b54fa-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b54fa-112">EXAMPLES</span></span>

### <span data-ttu-id="b54fa-113">1. példa: Az összes szolgáltató lekérte</span><span class="sxs-lookup"><span data-stu-id="b54fa-113">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="b54fa-114">Ez a parancs az összes OpenID Connect-szolgáltatót beveszi a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="b54fa-114">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="b54fa-115">2. példa: Szolgáltató lekérte azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="b54fa-115">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="b54fa-116">Ez a parancs az OICProvider01 azonosítóval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="b54fa-116">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="b54fa-117">3. példa: Szolgáltató lekérte egy név használatával</span><span class="sxs-lookup"><span data-stu-id="b54fa-117">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="b54fa-118">Ez a parancs a Contoso OpenID Connect Provider nevű szolgáltatót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b54fa-118">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="b54fa-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b54fa-119">PARAMETERS</span></span>

### <span data-ttu-id="b54fa-120">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b54fa-120">-Context</span></span>
<span data-ttu-id="b54fa-121">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="b54fa-121">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b54fa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b54fa-122">-DefaultProfile</span></span>
<span data-ttu-id="b54fa-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b54fa-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b54fa-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b54fa-124">-Name</span></span>
<span data-ttu-id="b54fa-125">A szolgáltató rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b54fa-125">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="b54fa-126">Ha megad egy nevet, ez a parancsmag kapja meg azt a szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="b54fa-126">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b54fa-127">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="b54fa-127">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="b54fa-128">Megadja annak a szolgáltatónak az azonosítóját, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="b54fa-128">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="b54fa-129">Ha megad egy azonosítót, ez a parancsmag kapja meg azt a szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="b54fa-129">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByOpenIdConnectProviderId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b54fa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b54fa-130">CommonParameters</span></span>
<span data-ttu-id="b54fa-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b54fa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b54fa-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b54fa-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b54fa-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b54fa-133">INPUTS</span></span>

### <span data-ttu-id="b54fa-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b54fa-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b54fa-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b54fa-135">System.String</span></span>

## <span data-ttu-id="b54fa-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b54fa-136">OUTPUTS</span></span>

### <span data-ttu-id="b54fa-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b54fa-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="b54fa-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b54fa-138">NOTES</span></span>

## <span data-ttu-id="b54fa-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b54fa-139">RELATED LINKS</span></span>

[<span data-ttu-id="b54fa-140">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b54fa-140">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="b54fa-141">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b54fa-141">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="b54fa-142">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b54fa-142">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


