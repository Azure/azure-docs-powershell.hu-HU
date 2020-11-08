---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 37144ab119eba4f19c3b34b2b32dfd28ff305677
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012223"
---
# <span data-ttu-id="ebb13-101">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="ebb13-101">New-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="ebb13-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ebb13-102">SYNOPSIS</span></span>
<span data-ttu-id="ebb13-103">OpenID csatlakoztatási szolgáltatót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ebb13-103">Creates an OpenID Connect provider.</span></span>

## <span data-ttu-id="ebb13-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ebb13-104">SYNTAX</span></span>

```
New-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 -Name <String> -MetadataEndpointUri <String> -ClientId <String> [-ClientSecret <String>]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebb13-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ebb13-105">DESCRIPTION</span></span>
<span data-ttu-id="ebb13-106">A **New-AzApiManagementOpenIdConnectProvider** parancsmag egy OpenID Connect-szolgáltatót hoz létre az Azure API-menedzsmentben.</span><span class="sxs-lookup"><span data-stu-id="ebb13-106">The **New-AzApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="ebb13-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ebb13-107">EXAMPLES</span></span>

### <span data-ttu-id="ebb13-108">1. példa: szolgáltató létrehozása</span><span class="sxs-lookup"><span data-stu-id="ebb13-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="ebb13-109">Ezzel a parancstal létrehoz egy OpenID Connect **Provider** nevű contoso OpenID Connect Provider szolgáltatót</span><span class="sxs-lookup"><span data-stu-id="ebb13-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="ebb13-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ebb13-110">PARAMETERS</span></span>

### <span data-ttu-id="ebb13-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="ebb13-111">-ClientId</span></span>
<span data-ttu-id="ebb13-112">A Fejlesztőeszközök konzol ügyfél-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ebb13-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="ebb13-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="ebb13-113">-ClientSecret</span></span>
<span data-ttu-id="ebb13-114">A fejlesztői konzol ügyfélprogramjának titkát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ebb13-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="ebb13-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ebb13-115">-Context</span></span>
<span data-ttu-id="ebb13-116">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="ebb13-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ebb13-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebb13-117">-DefaultProfile</span></span>
<span data-ttu-id="ebb13-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ebb13-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebb13-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="ebb13-119">-Description</span></span>
<span data-ttu-id="ebb13-120">Leírást ad meg.</span><span class="sxs-lookup"><span data-stu-id="ebb13-120">Specifies a description.</span></span>

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

### <span data-ttu-id="ebb13-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="ebb13-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="ebb13-122">Megadja a szolgáltató metaadat-végpontjának URI-jét.</span><span class="sxs-lookup"><span data-stu-id="ebb13-122">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="ebb13-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ebb13-123">-Name</span></span>
<span data-ttu-id="ebb13-124">A szolgáltató rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ebb13-124">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="ebb13-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="ebb13-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="ebb13-126">A szolgáltató AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ebb13-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="ebb13-127">Ha nem ad meg azonosítót, a parancsmag létrehoz egyet.</span><span class="sxs-lookup"><span data-stu-id="ebb13-127">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="ebb13-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebb13-128">CommonParameters</span></span>
<span data-ttu-id="ebb13-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ebb13-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebb13-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ebb13-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebb13-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebb13-131">INPUTS</span></span>

### <span data-ttu-id="ebb13-132">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ebb13-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ebb13-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ebb13-133">System.String</span></span>

## <span data-ttu-id="ebb13-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebb13-134">OUTPUTS</span></span>

### <span data-ttu-id="ebb13-135">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="ebb13-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="ebb13-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ebb13-136">NOTES</span></span>

## <span data-ttu-id="ebb13-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ebb13-137">RELATED LINKS</span></span>

[<span data-ttu-id="ebb13-138">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="ebb13-138">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="ebb13-139">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="ebb13-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="ebb13-140">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="ebb13-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


