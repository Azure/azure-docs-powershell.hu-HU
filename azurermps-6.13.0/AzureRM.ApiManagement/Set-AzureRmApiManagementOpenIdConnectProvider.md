---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6f568f27cf5b50cd517d8133578d6cf36060252f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492916"
---
# <span data-ttu-id="69ecf-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="69ecf-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="69ecf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="69ecf-103">Egy OpenID csatlakoztatási szolgáltatót módosít.</span><span class="sxs-lookup"><span data-stu-id="69ecf-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69ecf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69ecf-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69ecf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="69ecf-105">DESCRIPTION</span></span>
<span data-ttu-id="69ecf-106">A **set-AzureRmApiManagementOpenIdConnectProvider** parancsmag egy OpenID Connect-szolgáltatót módosít az Azure API-menedzsmentben.</span><span class="sxs-lookup"><span data-stu-id="69ecf-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="69ecf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="69ecf-107">EXAMPLES</span></span>

### <span data-ttu-id="69ecf-108">Példa 1: a szolgáltató titkos ügyfelének módosítása</span><span class="sxs-lookup"><span data-stu-id="69ecf-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="69ecf-109">Ez a parancs módosítja az azonosító OICProvicer01 szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="69ecf-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="69ecf-110">A parancs a szolgáltatóhoz tartozó ügyfél-titkot adja meg.</span><span class="sxs-lookup"><span data-stu-id="69ecf-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="69ecf-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69ecf-111">PARAMETERS</span></span>

### <span data-ttu-id="69ecf-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="69ecf-112">-ClientId</span></span>
<span data-ttu-id="69ecf-113">A Fejlesztőeszközök konzol ügyfél-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="69ecf-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="69ecf-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="69ecf-114">-ClientSecret</span></span>
<span data-ttu-id="69ecf-115">A fejlesztői konzol ügyfélprogramjának titkát adja meg.</span><span class="sxs-lookup"><span data-stu-id="69ecf-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="69ecf-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="69ecf-116">-Context</span></span>
<span data-ttu-id="69ecf-117">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="69ecf-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="69ecf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69ecf-118">-DefaultProfile</span></span>
<span data-ttu-id="69ecf-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69ecf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69ecf-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="69ecf-120">-Description</span></span>
<span data-ttu-id="69ecf-121">Leírást ad meg.</span><span class="sxs-lookup"><span data-stu-id="69ecf-121">Specifies a description.</span></span>

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

### <span data-ttu-id="69ecf-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="69ecf-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="69ecf-123">Megadja a szolgáltató metaadat-végpontjának URI-jét.</span><span class="sxs-lookup"><span data-stu-id="69ecf-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="69ecf-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="69ecf-124">-Name</span></span>
<span data-ttu-id="69ecf-125">A szolgáltató rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69ecf-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="69ecf-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="69ecf-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="69ecf-127">Annak a szolgáltatónak az AZONOSÍTÓját adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="69ecf-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="69ecf-128">Ha nem ad meg azonosítót, a parancsmag létrehoz egyet.</span><span class="sxs-lookup"><span data-stu-id="69ecf-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="69ecf-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69ecf-129">-PassThru</span></span>
<span data-ttu-id="69ecf-130">Jelzi, hogy ez a parancsmag a parancsmag által módosított **PsApiManagementOpenIdConnectProvider** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="69ecf-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ecf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ecf-131">CommonParameters</span></span>
<span data-ttu-id="69ecf-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69ecf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ecf-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69ecf-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ecf-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69ecf-134">INPUTS</span></span>

### <span data-ttu-id="69ecf-135">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="69ecf-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="69ecf-136">System. String</span><span class="sxs-lookup"><span data-stu-id="69ecf-136">System.String</span></span>

### <span data-ttu-id="69ecf-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="69ecf-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="69ecf-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69ecf-138">OUTPUTS</span></span>

### <span data-ttu-id="69ecf-139">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="69ecf-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="69ecf-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69ecf-140">NOTES</span></span>

## <span data-ttu-id="69ecf-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69ecf-141">RELATED LINKS</span></span>

[<span data-ttu-id="69ecf-142">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="69ecf-142">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="69ecf-143">Új – AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="69ecf-143">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="69ecf-144">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="69ecf-144">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


