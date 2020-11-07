---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: b6c8c0260e1f45b55dedca4d0a9f1f5ab3fed59a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665682"
---
# <span data-ttu-id="3ee35-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3ee35-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="3ee35-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ee35-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee35-103">Megkapja az OpenID Connect szolgáltatókat.</span><span class="sxs-lookup"><span data-stu-id="3ee35-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="3ee35-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ee35-104">SYNTAX</span></span>

### <span data-ttu-id="3ee35-105">GetAllOpenIdConnectProviders (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3ee35-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ee35-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="3ee35-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ee35-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="3ee35-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ee35-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ee35-108">DESCRIPTION</span></span>
<span data-ttu-id="3ee35-109">A **Get-AzApiManagementOpenIdConnectProvider** parancsmag OpenID Connect-szolgáltatókat kap az Azure API-menedzsmentben.</span><span class="sxs-lookup"><span data-stu-id="3ee35-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="3ee35-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3ee35-110">EXAMPLES</span></span>

### <span data-ttu-id="3ee35-111">Példa 1: az összes szolgáltató beszerzése</span><span class="sxs-lookup"><span data-stu-id="3ee35-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="3ee35-112">Ez a parancs az összes OpenID Connect szolgáltatót megkapja a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="3ee35-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="3ee35-113">2. példa: szolgáltató beszerzése azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="3ee35-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="3ee35-114">Ez a parancs a OICProvicer01 AZONOSÍTÓját tartalmazó szolgáltatót kapja.</span><span class="sxs-lookup"><span data-stu-id="3ee35-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="3ee35-115">3. példa: szolgáltató beszerzése név használatával</span><span class="sxs-lookup"><span data-stu-id="3ee35-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="3ee35-116">Ez a parancs a contoso OpenID Connect Provider nevű szolgáltatót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3ee35-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="3ee35-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ee35-117">PARAMETERS</span></span>

### <span data-ttu-id="3ee35-118">-Környezet</span><span class="sxs-lookup"><span data-stu-id="3ee35-118">-Context</span></span>
<span data-ttu-id="3ee35-119">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="3ee35-119">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee35-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee35-120">-DefaultProfile</span></span>
<span data-ttu-id="3ee35-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ee35-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ee35-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3ee35-122">-Name</span></span>
<span data-ttu-id="3ee35-123">A szolgáltató rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ee35-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="3ee35-124">Ha megad egy nevet, ez a parancsmag a szolgáltatót kapja.</span><span class="sxs-lookup"><span data-stu-id="3ee35-124">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="3ee35-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="3ee35-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="3ee35-126">Annak a szolgáltatónak az AZONOSÍTÓját adja meg, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="3ee35-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="3ee35-127">Ha azonosítót ad meg, ez a parancsmag a szolgáltatót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3ee35-127">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="3ee35-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee35-128">CommonParameters</span></span>
<span data-ttu-id="3ee35-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ee35-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee35-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ee35-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee35-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ee35-131">INPUTS</span></span>

### <span data-ttu-id="3ee35-132">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3ee35-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3ee35-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3ee35-133">System.String</span></span>

## <span data-ttu-id="3ee35-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ee35-134">OUTPUTS</span></span>

### <span data-ttu-id="3ee35-135">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3ee35-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="3ee35-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ee35-136">NOTES</span></span>

## <span data-ttu-id="3ee35-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ee35-137">RELATED LINKS</span></span>

[<span data-ttu-id="3ee35-138">Új – AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3ee35-138">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="3ee35-139">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3ee35-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="3ee35-140">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3ee35-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


