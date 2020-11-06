---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 088b88bcaa7f0d493552060c150e9d76a4b16c7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492422"
---
# <span data-ttu-id="27450-101">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="27450-101">New-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="27450-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27450-102">SYNOPSIS</span></span>
<span data-ttu-id="27450-103">OpenID csatlakoztatási szolgáltatót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="27450-103">Creates an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27450-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27450-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] -Name <String> -MetadataEndpointUri <String> -ClientId <String>
 [-ClientSecret <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27450-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="27450-105">DESCRIPTION</span></span>
<span data-ttu-id="27450-106">A **New-AzureRmApiManagementOpenIdConnectProvider** parancsmag egy OpenID Connect-szolgáltatót hoz létre az Azure API-menedzsmentben.</span><span class="sxs-lookup"><span data-stu-id="27450-106">The **New-AzureRmApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="27450-107">Példák</span><span class="sxs-lookup"><span data-stu-id="27450-107">EXAMPLES</span></span>

### <span data-ttu-id="27450-108">1. példa: szolgáltató létrehozása</span><span class="sxs-lookup"><span data-stu-id="27450-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="27450-109">Ezzel a parancstal létrehoz egy OpenID Connect **Provider** nevű contoso OpenID Connect Provider szolgáltatót</span><span class="sxs-lookup"><span data-stu-id="27450-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="27450-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27450-110">PARAMETERS</span></span>

### <span data-ttu-id="27450-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="27450-111">-ClientId</span></span>
<span data-ttu-id="27450-112">A Fejlesztőeszközök konzol ügyfél-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="27450-112">Specifies the client ID of the developer console.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27450-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="27450-113">-ClientSecret</span></span>
<span data-ttu-id="27450-114">A fejlesztői konzol ügyfélprogramjának titkát adja meg.</span><span class="sxs-lookup"><span data-stu-id="27450-114">Specifies the client secret of the developer console.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27450-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="27450-115">-Context</span></span>
<span data-ttu-id="27450-116">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="27450-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27450-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27450-117">-DefaultProfile</span></span>
<span data-ttu-id="27450-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27450-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27450-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="27450-119">-Description</span></span>
<span data-ttu-id="27450-120">Leírást ad meg.</span><span class="sxs-lookup"><span data-stu-id="27450-120">Specifies a description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27450-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="27450-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="27450-122">Megadja a szolgáltató metaadat-végpontjának URI-jét.</span><span class="sxs-lookup"><span data-stu-id="27450-122">Specifies a metadata endpoint URI of the provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27450-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="27450-123">-Name</span></span>
<span data-ttu-id="27450-124">A szolgáltató rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="27450-124">Specifies a friendly name for the provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27450-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="27450-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="27450-126">A szolgáltató AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="27450-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="27450-127">Ha nem ad meg azonosítót, a parancsmag létrehoz egyet.</span><span class="sxs-lookup"><span data-stu-id="27450-127">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27450-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27450-128">CommonParameters</span></span>
<span data-ttu-id="27450-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27450-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27450-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27450-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27450-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27450-131">INPUTS</span></span>

### <span data-ttu-id="27450-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="27450-132">None</span></span>
<span data-ttu-id="27450-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="27450-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="27450-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27450-134">OUTPUTS</span></span>

### <span data-ttu-id="27450-135">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="27450-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="27450-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27450-136">NOTES</span></span>

## <span data-ttu-id="27450-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27450-137">RELATED LINKS</span></span>

[<span data-ttu-id="27450-138">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="27450-138">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="27450-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="27450-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="27450-140">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="27450-140">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


