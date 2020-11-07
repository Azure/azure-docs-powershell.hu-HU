---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 880c44e3edf8a5d2c95144d2af8910e73d366192
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667931"
---
# <span data-ttu-id="d6f0f-101">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d6f0f-101">Set-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="d6f0f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6f0f-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f0f-103">Egy OpenID csatlakoztatási szolgáltatót módosít.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-103">Modifies an OpenID Connect provider.</span></span>

## <span data-ttu-id="d6f0f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6f0f-104">SYNTAX</span></span>

```
Set-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>] [-ClientSecret <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6f0f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6f0f-105">DESCRIPTION</span></span>
<span data-ttu-id="d6f0f-106">A **set-AzApiManagementOpenIdConnectProvider** parancsmag egy OpenID Connect-szolgáltatót módosít az Azure API-menedzsmentben.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-106">The **Set-AzApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="d6f0f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d6f0f-107">EXAMPLES</span></span>

### <span data-ttu-id="d6f0f-108">Példa 1: a szolgáltató titkos ügyfelének módosítása</span><span class="sxs-lookup"><span data-stu-id="d6f0f-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="d6f0f-109">Ez a parancs módosítja az azonosító OICProvider01 szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-109">This command modifies the provider that has the ID OICProvider01.</span></span>
<span data-ttu-id="d6f0f-110">A parancs a szolgáltatóhoz tartozó ügyfél-titkot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="d6f0f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6f0f-111">PARAMETERS</span></span>

### <span data-ttu-id="d6f0f-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="d6f0f-112">-ClientId</span></span>
<span data-ttu-id="d6f0f-113">A Fejlesztőeszközök konzol ügyfél-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="d6f0f-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="d6f0f-114">-ClientSecret</span></span>
<span data-ttu-id="d6f0f-115">A fejlesztői konzol ügyfélprogramjának titkát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="d6f0f-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d6f0f-116">-Context</span></span>
<span data-ttu-id="d6f0f-117">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d6f0f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f0f-118">-DefaultProfile</span></span>
<span data-ttu-id="d6f0f-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6f0f-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="d6f0f-120">-Description</span></span>
<span data-ttu-id="d6f0f-121">Leírást ad meg.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-121">Specifies a description.</span></span>

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

### <span data-ttu-id="d6f0f-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="d6f0f-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="d6f0f-123">Megadja a szolgáltató metaadat-végpontjának URI-jét.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="d6f0f-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d6f0f-124">-Name</span></span>
<span data-ttu-id="d6f0f-125">A szolgáltató rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="d6f0f-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="d6f0f-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="d6f0f-127">Annak a szolgáltatónak az AZONOSÍTÓját adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="d6f0f-128">Ha nem ad meg azonosítót, a parancsmag létrehoz egyet.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="d6f0f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6f0f-129">-PassThru</span></span>
<span data-ttu-id="d6f0f-130">Jelzi, hogy ez a parancsmag a parancsmag által módosított **PsApiManagementOpenIdConnectProvider** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d6f0f-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d6f0f-131">-Confirm</span></span>
<span data-ttu-id="d6f0f-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f0f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6f0f-133">-WhatIf</span></span>
<span data-ttu-id="d6f0f-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6f0f-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f0f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f0f-136">CommonParameters</span></span>
<span data-ttu-id="d6f0f-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6f0f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f0f-138">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d6f0f-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f0f-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6f0f-139">INPUTS</span></span>

### <span data-ttu-id="d6f0f-140">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d6f0f-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d6f0f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d6f0f-141">System.String</span></span>

### <span data-ttu-id="d6f0f-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d6f0f-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d6f0f-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6f0f-143">OUTPUTS</span></span>

### <span data-ttu-id="d6f0f-144">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d6f0f-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="d6f0f-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6f0f-145">NOTES</span></span>

## <span data-ttu-id="d6f0f-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6f0f-146">RELATED LINKS</span></span>

[<span data-ttu-id="d6f0f-147">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d6f0f-147">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="d6f0f-148">Új – AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d6f0f-148">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="d6f0f-149">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d6f0f-149">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)


