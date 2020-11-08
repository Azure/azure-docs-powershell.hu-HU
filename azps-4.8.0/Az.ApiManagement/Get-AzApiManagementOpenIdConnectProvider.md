---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6968b4ea1b222d0f046611f10e65f8073a4ba86a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018017"
---
# <span data-ttu-id="863dd-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="863dd-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="863dd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="863dd-102">SYNOPSIS</span></span>
<span data-ttu-id="863dd-103">Megkapja az OpenID Connect szolgáltatókat.</span><span class="sxs-lookup"><span data-stu-id="863dd-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="863dd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="863dd-104">SYNTAX</span></span>

### <span data-ttu-id="863dd-105">GetAllOpenIdConnectProviders (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="863dd-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="863dd-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="863dd-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="863dd-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="863dd-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="863dd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="863dd-108">DESCRIPTION</span></span>
<span data-ttu-id="863dd-109">A **Get-AzApiManagementOpenIdConnectProvider** parancsmag OpenID Connect-szolgáltatókat kap az Azure API-menedzsmentben.</span><span class="sxs-lookup"><span data-stu-id="863dd-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>
<span data-ttu-id="863dd-110">A ClientSecret nem fog szerepelni az eredmény részletei között.</span><span class="sxs-lookup"><span data-stu-id="863dd-110">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="863dd-111">Az ügyfél titkának beszerzéséhez használja a **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span><span class="sxs-lookup"><span data-stu-id="863dd-111">To get client secret, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span></span>

## <span data-ttu-id="863dd-112">Példák</span><span class="sxs-lookup"><span data-stu-id="863dd-112">EXAMPLES</span></span>

### <span data-ttu-id="863dd-113">Példa 1: az összes szolgáltató beszerzése</span><span class="sxs-lookup"><span data-stu-id="863dd-113">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="863dd-114">Ez a parancs az összes OpenID Connect szolgáltatót megkapja a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="863dd-114">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="863dd-115">2. példa: szolgáltató beszerzése azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="863dd-115">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="863dd-116">Ez a parancs a OICProvider01 AZONOSÍTÓját tartalmazó szolgáltatót kapja.</span><span class="sxs-lookup"><span data-stu-id="863dd-116">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="863dd-117">3. példa: szolgáltató beszerzése név használatával</span><span class="sxs-lookup"><span data-stu-id="863dd-117">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="863dd-118">Ez a parancs a contoso OpenID Connect Provider nevű szolgáltatót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="863dd-118">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="863dd-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="863dd-119">PARAMETERS</span></span>

### <span data-ttu-id="863dd-120">-Környezet</span><span class="sxs-lookup"><span data-stu-id="863dd-120">-Context</span></span>
<span data-ttu-id="863dd-121">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="863dd-121">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="863dd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="863dd-122">-DefaultProfile</span></span>
<span data-ttu-id="863dd-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="863dd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="863dd-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="863dd-124">-Name</span></span>
<span data-ttu-id="863dd-125">A szolgáltató rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="863dd-125">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="863dd-126">Ha megad egy nevet, ez a parancsmag a szolgáltatót kapja.</span><span class="sxs-lookup"><span data-stu-id="863dd-126">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="863dd-127">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="863dd-127">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="863dd-128">Annak a szolgáltatónak az AZONOSÍTÓját adja meg, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="863dd-128">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="863dd-129">Ha azonosítót ad meg, ez a parancsmag a szolgáltatót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="863dd-129">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="863dd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="863dd-130">CommonParameters</span></span>
<span data-ttu-id="863dd-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="863dd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="863dd-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="863dd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="863dd-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="863dd-133">INPUTS</span></span>

### <span data-ttu-id="863dd-134">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="863dd-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="863dd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="863dd-135">System.String</span></span>

## <span data-ttu-id="863dd-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="863dd-136">OUTPUTS</span></span>

### <span data-ttu-id="863dd-137">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="863dd-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="863dd-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="863dd-138">NOTES</span></span>

## <span data-ttu-id="863dd-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="863dd-139">RELATED LINKS</span></span>

[<span data-ttu-id="863dd-140">Új – AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="863dd-140">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="863dd-141">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="863dd-141">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="863dd-142">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="863dd-142">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


