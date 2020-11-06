---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: f890236907ea0a717245d9345be276a6ccf04b8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499263"
---
# <span data-ttu-id="e79fb-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="e79fb-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="e79fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e79fb-102">SYNOPSIS</span></span>
<span data-ttu-id="e79fb-103">Egy OpenID csatlakoztatási szolgáltatót módosít.</span><span class="sxs-lookup"><span data-stu-id="e79fb-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e79fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e79fb-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e79fb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e79fb-105">DESCRIPTION</span></span>
<span data-ttu-id="e79fb-106">A **set-AzureRmApiManagementOpenIdConnectProvider** parancsmag egy OpenID Connect-szolgáltatót módosít az Azure API-menedzsmentben.</span><span class="sxs-lookup"><span data-stu-id="e79fb-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="e79fb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e79fb-107">EXAMPLES</span></span>

### <span data-ttu-id="e79fb-108">Példa 1: a szolgáltató titkos ügyfelének módosítása</span><span class="sxs-lookup"><span data-stu-id="e79fb-108">Example 1: Change the client secret for a provider</span></span>
```
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="e79fb-109">Ez a parancs módosítja az azonosító OICProvicer01 szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="e79fb-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="e79fb-110">A parancs a szolgáltatóhoz tartozó ügyfél-titkot adja meg.</span><span class="sxs-lookup"><span data-stu-id="e79fb-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="e79fb-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e79fb-111">PARAMETERS</span></span>

### <span data-ttu-id="e79fb-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="e79fb-112">-ClientId</span></span>
<span data-ttu-id="e79fb-113">A Fejlesztőeszközök konzol ügyfél-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e79fb-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="e79fb-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="e79fb-114">-ClientSecret</span></span>
<span data-ttu-id="e79fb-115">A fejlesztői konzol ügyfélprogramjának titkát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e79fb-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="e79fb-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e79fb-116">-Context</span></span>
<span data-ttu-id="e79fb-117">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="e79fb-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e79fb-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="e79fb-118">-Description</span></span>
<span data-ttu-id="e79fb-119">Leírást ad meg.</span><span class="sxs-lookup"><span data-stu-id="e79fb-119">Specifies a description.</span></span>

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

### <span data-ttu-id="e79fb-120">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="e79fb-120">-MetadataEndpointUri</span></span>
<span data-ttu-id="e79fb-121">Megadja a szolgáltató metaadat-végpontjának URI-jét.</span><span class="sxs-lookup"><span data-stu-id="e79fb-121">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="e79fb-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e79fb-122">-Name</span></span>
<span data-ttu-id="e79fb-123">A szolgáltató rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e79fb-123">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="e79fb-124">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="e79fb-124">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="e79fb-125">Annak a szolgáltatónak az AZONOSÍTÓját adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="e79fb-125">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="e79fb-126">Ha nem ad meg azonosítót, a parancsmag létrehoz egyet.</span><span class="sxs-lookup"><span data-stu-id="e79fb-126">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="e79fb-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e79fb-127">-PassThru</span></span>
<span data-ttu-id="e79fb-128">Jelzi, hogy ez a parancsmag a parancsmag által módosított **PsApiManagementOpenIdConnectProvider** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e79fb-128">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e79fb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e79fb-129">-DefaultProfile</span></span>
<span data-ttu-id="e79fb-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e79fb-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e79fb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e79fb-131">CommonParameters</span></span>
<span data-ttu-id="e79fb-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e79fb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e79fb-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e79fb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e79fb-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e79fb-134">INPUTS</span></span>

## <span data-ttu-id="e79fb-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e79fb-135">OUTPUTS</span></span>

### <span data-ttu-id="e79fb-136">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="e79fb-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="e79fb-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e79fb-137">NOTES</span></span>

## <span data-ttu-id="e79fb-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e79fb-138">RELATED LINKS</span></span>

[<span data-ttu-id="e79fb-139">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="e79fb-139">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="e79fb-140">Új – AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="e79fb-140">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="e79fb-141">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="e79fb-141">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


