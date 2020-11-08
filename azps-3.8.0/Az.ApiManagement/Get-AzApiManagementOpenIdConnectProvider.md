---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: b39ae66a5881acca72143274c479685ef1282854
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013877"
---
# <span data-ttu-id="0c7f5-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0c7f5-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="0c7f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0c7f5-102">SYNOPSIS</span></span>
<span data-ttu-id="0c7f5-103">Megkapja az OpenID Connect szolgáltatókat.</span><span class="sxs-lookup"><span data-stu-id="0c7f5-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="0c7f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0c7f5-104">SYNTAX</span></span>

### <span data-ttu-id="0c7f5-105">GetAllOpenIdConnectProviders (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0c7f5-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c7f5-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="0c7f5-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c7f5-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="0c7f5-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c7f5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0c7f5-108">DESCRIPTION</span></span>
<span data-ttu-id="0c7f5-109">A **Get-AzApiManagementOpenIdConnectProvider** parancsmag OpenID Connect-szolgáltatókat kap az Azure API-menedzsmentben.</span><span class="sxs-lookup"><span data-stu-id="0c7f5-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="0c7f5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0c7f5-110">EXAMPLES</span></span>

### <span data-ttu-id="0c7f5-111">Példa 1: az összes szolgáltató beszerzése</span><span class="sxs-lookup"><span data-stu-id="0c7f5-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="0c7f5-112">Ez a parancs az összes OpenID Connect szolgáltatót megkapja a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="0c7f5-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="0c7f5-113">2. példa: szolgáltató beszerzése azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="0c7f5-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="0c7f5-114">Ez a parancs a OICProvider01 AZONOSÍTÓját tartalmazó szolgáltatót kapja.</span><span class="sxs-lookup"><span data-stu-id="0c7f5-114">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="0c7f5-115">3. példa: szolgáltató beszerzése név használatával</span><span class="sxs-lookup"><span data-stu-id="0c7f5-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="0c7f5-116">Ez a parancs a contoso OpenID Connect Provider nevű szolgáltatót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0c7f5-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="0c7f5-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0c7f5-117">PARAMETERS</span></span>

### <span data-ttu-id="0c7f5-118">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0c7f5-118">-Context</span></span>
<span data-ttu-id="0c7f5-119">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="0c7f5-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0c7f5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c7f5-120">-DefaultProfile</span></span>
<span data-ttu-id="0c7f5-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c7f5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c7f5-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0c7f5-122">-Name</span></span>
<span data-ttu-id="0c7f5-123">A szolgáltató rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c7f5-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="0c7f5-124">Ha megad egy nevet, ez a parancsmag a szolgáltatót kapja.</span><span class="sxs-lookup"><span data-stu-id="0c7f5-124">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="0c7f5-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="0c7f5-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="0c7f5-126">Annak a szolgáltatónak az AZONOSÍTÓját adja meg, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="0c7f5-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="0c7f5-127">Ha azonosítót ad meg, ez a parancsmag a szolgáltatót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0c7f5-127">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="0c7f5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c7f5-128">CommonParameters</span></span>
<span data-ttu-id="0c7f5-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0c7f5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c7f5-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0c7f5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c7f5-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c7f5-131">INPUTS</span></span>

### <span data-ttu-id="0c7f5-132">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0c7f5-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0c7f5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0c7f5-133">System.String</span></span>

## <span data-ttu-id="0c7f5-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c7f5-134">OUTPUTS</span></span>

### <span data-ttu-id="0c7f5-135">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0c7f5-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="0c7f5-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0c7f5-136">NOTES</span></span>

## <span data-ttu-id="0c7f5-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c7f5-137">RELATED LINKS</span></span>

[<span data-ttu-id="0c7f5-138">Új – AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0c7f5-138">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="0c7f5-139">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0c7f5-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="0c7f5-140">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0c7f5-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


