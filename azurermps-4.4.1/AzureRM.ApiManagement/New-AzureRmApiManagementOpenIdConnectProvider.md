---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: f008d21e1d1d3f2aba7c87255fa7c95074bca532
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498043"
---
# <span data-ttu-id="50a47-101">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="50a47-101">New-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="50a47-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="50a47-102">SYNOPSIS</span></span>
<span data-ttu-id="50a47-103">OpenID csatlakoztatási szolgáltatót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="50a47-103">Creates an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50a47-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="50a47-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] -Name <String> -MetadataEndpointUri <String> -ClientId <String>
 [-ClientSecret <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50a47-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="50a47-105">DESCRIPTION</span></span>
<span data-ttu-id="50a47-106">A **New-AzureRmApiManagementOpenIdConnectProvider** parancsmag egy OpenID Connect-szolgáltatót hoz létre az Azure API-menedzsmentben.</span><span class="sxs-lookup"><span data-stu-id="50a47-106">The **New-AzureRmApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="50a47-107">Példák</span><span class="sxs-lookup"><span data-stu-id="50a47-107">EXAMPLES</span></span>

### <span data-ttu-id="50a47-108">1. példa: szolgáltató létrehozása</span><span class="sxs-lookup"><span data-stu-id="50a47-108">Example 1: Create a provider</span></span>
```
PS C:\>New-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="50a47-109">Ezzel a parancstal létrehoz egy OpenID Connect **Provider** nevű contoso OpenID Connect Provider szolgáltatót</span><span class="sxs-lookup"><span data-stu-id="50a47-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="50a47-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="50a47-110">PARAMETERS</span></span>

### <span data-ttu-id="50a47-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="50a47-111">-ClientId</span></span>
<span data-ttu-id="50a47-112">A Fejlesztőeszközök konzol ügyfél-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="50a47-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="50a47-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="50a47-113">-ClientSecret</span></span>
<span data-ttu-id="50a47-114">A fejlesztői konzol ügyfélprogramjának titkát adja meg.</span><span class="sxs-lookup"><span data-stu-id="50a47-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="50a47-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="50a47-115">-Context</span></span>
<span data-ttu-id="50a47-116">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="50a47-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="50a47-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="50a47-117">-Description</span></span>
<span data-ttu-id="50a47-118">Leírást ad meg.</span><span class="sxs-lookup"><span data-stu-id="50a47-118">Specifies a description.</span></span>

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

### <span data-ttu-id="50a47-119">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="50a47-119">-MetadataEndpointUri</span></span>
<span data-ttu-id="50a47-120">Megadja a szolgáltató metaadat-végpontjának URI-jét.</span><span class="sxs-lookup"><span data-stu-id="50a47-120">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="50a47-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="50a47-121">-Name</span></span>
<span data-ttu-id="50a47-122">A szolgáltató rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="50a47-122">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="50a47-123">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="50a47-123">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="50a47-124">A szolgáltató AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="50a47-124">Specifies an ID for the provider.</span></span>
<span data-ttu-id="50a47-125">Ha nem ad meg azonosítót, a parancsmag létrehoz egyet.</span><span class="sxs-lookup"><span data-stu-id="50a47-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="50a47-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50a47-126">-DefaultProfile</span></span>
<span data-ttu-id="50a47-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="50a47-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50a47-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50a47-128">CommonParameters</span></span>
<span data-ttu-id="50a47-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="50a47-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50a47-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50a47-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50a47-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="50a47-131">INPUTS</span></span>

## <span data-ttu-id="50a47-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50a47-132">OUTPUTS</span></span>

### <span data-ttu-id="50a47-133">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="50a47-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="50a47-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="50a47-134">NOTES</span></span>

## <span data-ttu-id="50a47-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50a47-135">RELATED LINKS</span></span>

[<span data-ttu-id="50a47-136">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="50a47-136">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="50a47-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="50a47-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="50a47-138">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="50a47-138">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


