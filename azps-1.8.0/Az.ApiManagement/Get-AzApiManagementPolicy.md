---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
ms.openlocfilehash: 0da4e2168ccc7f5a62aa4265af3b7823dd4cb050
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665678"
---
# <span data-ttu-id="27c2d-101">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="27c2d-101">Get-AzApiManagementPolicy</span></span>

## <span data-ttu-id="27c2d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="27c2d-103">Megkapja a megadott hatókör-házirendet.</span><span class="sxs-lookup"><span data-stu-id="27c2d-103">Gets the specified scope policy.</span></span>

## <span data-ttu-id="27c2d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27c2d-104">SYNTAX</span></span>

### <span data-ttu-id="27c2d-105">GetTenantLevel (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="27c2d-105">GetTenantLevel (Default)</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27c2d-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="27c2d-106">GetProductLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27c2d-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="27c2d-107">GetApiLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27c2d-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="27c2d-108">GetOperationLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27c2d-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="27c2d-109">DESCRIPTION</span></span>
<span data-ttu-id="27c2d-110">A **Get-AzApiManagementPolicy** parancsmag a megadott hatóköri házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="27c2d-110">The **Get-AzApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="27c2d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="27c2d-111">EXAMPLES</span></span>

### <span data-ttu-id="27c2d-112">Példa 1: a bérlői szint házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="27c2d-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="27c2d-113">Ez a parancs bérlői szintű házirendet kap, és egy tenantpolicy.xml nevű fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="27c2d-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="27c2d-114">2. példa: a termékspecifikus házirend beszerzése</span><span class="sxs-lookup"><span data-stu-id="27c2d-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="27c2d-115">Ez a parancs a Product-scope Policy házirendet kapja meg</span><span class="sxs-lookup"><span data-stu-id="27c2d-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="27c2d-116">3. példa: az API-hatókörök házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="27c2d-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="27c2d-117">Ez a parancs API-hatóköri házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="27c2d-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="27c2d-118">Példa 4: a művelet-hatókör házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="27c2d-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="27c2d-119">Ez a parancs a művelet hatóköre házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="27c2d-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="27c2d-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27c2d-120">PARAMETERS</span></span>

### <span data-ttu-id="27c2d-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="27c2d-121">-ApiId</span></span>
<span data-ttu-id="27c2d-122">A meglévő API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="27c2d-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="27c2d-123">Ha ezt a paramétert adja meg, a parancsmag az API-scope házirendet adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="27c2d-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27c2d-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="27c2d-124">-ApiRevision</span></span>
<span data-ttu-id="27c2d-125">Az API-módosítás azonosítója</span><span class="sxs-lookup"><span data-stu-id="27c2d-125">Identifier of API Revision.</span></span> <span data-ttu-id="27c2d-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="27c2d-126">This parameter is optional.</span></span> <span data-ttu-id="27c2d-127">Ha nem adja meg, akkor a rendszer az aktuális API-verzióból olvassa be a házirendet.</span><span class="sxs-lookup"><span data-stu-id="27c2d-127">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27c2d-128">-Környezet</span><span class="sxs-lookup"><span data-stu-id="27c2d-128">-Context</span></span>
<span data-ttu-id="27c2d-129">A **PsApiManagementContext** példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="27c2d-129">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="27c2d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27c2d-130">-DefaultProfile</span></span>
<span data-ttu-id="27c2d-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27c2d-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27c2d-132">-Force</span><span class="sxs-lookup"><span data-stu-id="27c2d-132">-Force</span></span>
<span data-ttu-id="27c2d-133">ps_force</span><span class="sxs-lookup"><span data-stu-id="27c2d-133">ps_force</span></span>

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

### <span data-ttu-id="27c2d-134">Formátumú</span><span class="sxs-lookup"><span data-stu-id="27c2d-134">-Format</span></span>
<span data-ttu-id="27c2d-135">Az API-kezelési házirend formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="27c2d-135">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="27c2d-136">A paraméter alapértelmezett értéke az "Application/vnd. MS-az-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="27c2d-136">The default value for this parameter is "application/vnd.ms-az-apim.policy+xml".</span></span>

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

### <span data-ttu-id="27c2d-137">-OperationId</span><span class="sxs-lookup"><span data-stu-id="27c2d-137">-OperationId</span></span>
<span data-ttu-id="27c2d-138">A meglévő API-művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="27c2d-138">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="27c2d-139">Ha ezt a paramétert a *ApiId* -ban adja meg, a parancsmag a műveleti hatókör házirendjét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="27c2d-139">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27c2d-140">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="27c2d-140">-ProductId</span></span>
<span data-ttu-id="27c2d-141">Egy meglévő szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="27c2d-141">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="27c2d-142">Ha ezt a paramétert adja meg, a parancsmag a termékspecifikus házirendet adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="27c2d-142">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27c2d-143">-Saven</span><span class="sxs-lookup"><span data-stu-id="27c2d-143">-SaveAs</span></span>
<span data-ttu-id="27c2d-144">Annak a fájlnak az elérési útját adja meg, ahová menteni szeretné az eredményt.</span><span class="sxs-lookup"><span data-stu-id="27c2d-144">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="27c2d-145">Ha nem adja meg ezt a paramétert, az eredmény a folyamat csípése.</span><span class="sxs-lookup"><span data-stu-id="27c2d-145">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="27c2d-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="27c2d-146">-Confirm</span></span>
<span data-ttu-id="27c2d-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="27c2d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27c2d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27c2d-148">-WhatIf</span></span>
<span data-ttu-id="27c2d-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="27c2d-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27c2d-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="27c2d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27c2d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27c2d-151">CommonParameters</span></span>
<span data-ttu-id="27c2d-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27c2d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27c2d-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27c2d-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27c2d-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27c2d-154">INPUTS</span></span>

### <span data-ttu-id="27c2d-155">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="27c2d-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="27c2d-156">System. String</span><span class="sxs-lookup"><span data-stu-id="27c2d-156">System.String</span></span>

### <span data-ttu-id="27c2d-157">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="27c2d-157">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="27c2d-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27c2d-158">OUTPUTS</span></span>

### <span data-ttu-id="27c2d-159">System. String</span><span class="sxs-lookup"><span data-stu-id="27c2d-159">System.String</span></span>

## <span data-ttu-id="27c2d-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27c2d-160">NOTES</span></span>

## <span data-ttu-id="27c2d-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27c2d-161">RELATED LINKS</span></span>

[<span data-ttu-id="27c2d-162">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="27c2d-162">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)

[<span data-ttu-id="27c2d-163">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="27c2d-163">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


