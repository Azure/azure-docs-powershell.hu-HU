---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: b5e51891f82b2a12f42fac3a1535f974912ca1dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496687"
---
# <span data-ttu-id="cd2f6-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cd2f6-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="cd2f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd2f6-102">SYNOPSIS</span></span>
<span data-ttu-id="cd2f6-103">A backend frissítése</span><span class="sxs-lookup"><span data-stu-id="cd2f6-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd2f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd2f6-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd2f6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd2f6-105">DESCRIPTION</span></span>
<span data-ttu-id="cd2f6-106">Egy meglévő backend frissítése az API-kezelésben.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="cd2f6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cd2f6-107">EXAMPLES</span></span>

### <span data-ttu-id="cd2f6-108">A backend 123 leírásának frissítése</span><span class="sxs-lookup"><span data-stu-id="cd2f6-108">Updates the Description of the Backend 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="cd2f6-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd2f6-109">PARAMETERS</span></span>

### <span data-ttu-id="cd2f6-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="cd2f6-110">-BackendId</span></span>
<span data-ttu-id="cd2f6-111">Új backend-azonosító.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-111">Identifier of new backend.</span></span>
<span data-ttu-id="cd2f6-112">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-112">This parameter is required.</span></span>

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

### <span data-ttu-id="cd2f6-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="cd2f6-113">-Context</span></span>
<span data-ttu-id="cd2f6-114">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="cd2f6-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-115">This parameter is required.</span></span>

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

### <span data-ttu-id="cd2f6-116">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="cd2f6-116">-Credential</span></span>
<span data-ttu-id="cd2f6-117">Hitelesítő adatok, amelyeket a háttérben való beszélgetés során használni kell.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="cd2f6-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-118">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd2f6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd2f6-119">-DefaultProfile</span></span>
<span data-ttu-id="cd2f6-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="cd2f6-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="cd2f6-121">-Description</span></span>
<span data-ttu-id="cd2f6-122">A backend leírása.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-122">Backend Description.</span></span>
<span data-ttu-id="cd2f6-123">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="cd2f6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd2f6-124">-PassThru</span></span>
<span data-ttu-id="cd2f6-125">Jelzi, hogy ez a parancsmag a parancsmag által módosított  **PsApiManagementBackend** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd2f6-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="cd2f6-126">-Protocol</span></span>
<span data-ttu-id="cd2f6-127">Backend kommunikációs protokoll (http vagy SOAP).</span><span class="sxs-lookup"><span data-stu-id="cd2f6-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="cd2f6-128">Ez a paraméter nem kötelező</span><span class="sxs-lookup"><span data-stu-id="cd2f6-128">This parameter is optional</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd2f6-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="cd2f6-129">-Proxy</span></span>
<span data-ttu-id="cd2f6-130">A munkaablakba való küldéskor használandó proxykiszolgáló-adatok.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="cd2f6-131">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-131">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd2f6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd2f6-132">-ResourceId</span></span>
<span data-ttu-id="cd2f6-133">Az erőforrás felügyeleti URI-ja külső rendszerben</span><span class="sxs-lookup"><span data-stu-id="cd2f6-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="cd2f6-134">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-134">This parameter is optional.</span></span>
<span data-ttu-id="cd2f6-135">Ez az URL-cím lehet a logikai alkalmazások, a függvények és az API-alkalmazások ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="cd2f6-136">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="cd2f6-136">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="cd2f6-137">Szeretné-e kihagyni a tanúsítványláncot az érvényesítést, ha a háttérrel beszél.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-137">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="cd2f6-138">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-138">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd2f6-139">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="cd2f6-139">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="cd2f6-140">Szeretné-e kihagyni a tanúsítvány nevének érvényesítését, amikor a háttérben beszél.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-140">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="cd2f6-141">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-141">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd2f6-142">-Cím</span><span class="sxs-lookup"><span data-stu-id="cd2f6-142">-Title</span></span>
<span data-ttu-id="cd2f6-143">A backend címe.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-143">Backend Title.</span></span>
<span data-ttu-id="cd2f6-144">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="cd2f6-145">-URL</span><span class="sxs-lookup"><span data-stu-id="cd2f6-145">-Url</span></span>
<span data-ttu-id="cd2f6-146">A backend futásidejű URL-címe.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-146">Runtime Url for the Backend.</span></span>
<span data-ttu-id="cd2f6-147">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="cd2f6-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cd2f6-148">-Confirm</span></span>
<span data-ttu-id="cd2f6-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd2f6-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd2f6-150">-WhatIf</span></span>
<span data-ttu-id="cd2f6-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd2f6-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd2f6-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd2f6-153">CommonParameters</span></span>
<span data-ttu-id="cd2f6-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd2f6-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd2f6-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd2f6-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd2f6-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd2f6-156">INPUTS</span></span>

### <span data-ttu-id="cd2f6-157">Nincs</span><span class="sxs-lookup"><span data-stu-id="cd2f6-157">None</span></span>
<span data-ttu-id="cd2f6-158">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cd2f6-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd2f6-159">OUTPUTS</span></span>

### <span data-ttu-id="cd2f6-160">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cd2f6-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="cd2f6-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd2f6-161">NOTES</span></span>

## <span data-ttu-id="cd2f6-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd2f6-162">RELATED LINKS</span></span>

[<span data-ttu-id="cd2f6-163">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cd2f6-163">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="cd2f6-164">Új – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cd2f6-164">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="cd2f6-165">Új – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="cd2f6-165">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="cd2f6-166">Új – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="cd2f6-166">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="cd2f6-167">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cd2f6-167">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
