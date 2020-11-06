---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: fcf88fcb9b54adec01b8a04b50f557b6a74e7ca8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492093"
---
# <span data-ttu-id="29864-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="29864-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="29864-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29864-102">SYNOPSIS</span></span>
<span data-ttu-id="29864-103">Megkapja a megadott hatókör-házirendet.</span><span class="sxs-lookup"><span data-stu-id="29864-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29864-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29864-104">SYNTAX</span></span>

### <span data-ttu-id="29864-105">GetTenantLevel (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="29864-105">GetTenantLevel (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29864-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="29864-106">GetProductLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29864-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="29864-107">GetApiLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29864-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="29864-108">GetOperationLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29864-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="29864-109">DESCRIPTION</span></span>
<span data-ttu-id="29864-110">A **Get-AzureRmApiManagementPolicy** parancsmag a megadott hatóköri házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="29864-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="29864-111">Példák</span><span class="sxs-lookup"><span data-stu-id="29864-111">EXAMPLES</span></span>

### <span data-ttu-id="29864-112">Példa 1: a bérlői szint házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="29864-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="29864-113">Ez a parancs bérlői szintű házirendet kap, és egy tenantpolicy.xml nevű fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="29864-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="29864-114">2. példa: a termékspecifikus házirend beszerzése</span><span class="sxs-lookup"><span data-stu-id="29864-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="29864-115">Ez a parancs a Product-scope Policy házirendet kapja meg</span><span class="sxs-lookup"><span data-stu-id="29864-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="29864-116">3. példa: az API-hatókörök házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="29864-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="29864-117">Ez a parancs API-hatóköri házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="29864-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="29864-118">Példa 4: a művelet-hatókör házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="29864-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="29864-119">Ez a parancs a művelet hatóköre házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="29864-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="29864-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29864-120">PARAMETERS</span></span>

### <span data-ttu-id="29864-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="29864-121">-ApiId</span></span>
<span data-ttu-id="29864-122">A meglévő API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="29864-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="29864-123">Ha ezt a paramétert adja meg, a parancsmag az API-scope házirendet adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="29864-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

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

### <span data-ttu-id="29864-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="29864-124">-ApiRevision</span></span>
<span data-ttu-id="29864-125">Az API-módosítás azonosítója</span><span class="sxs-lookup"><span data-stu-id="29864-125">Identifier of API Revision.</span></span> <span data-ttu-id="29864-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="29864-126">This parameter is optional.</span></span> <span data-ttu-id="29864-127">Ha nem adja meg, akkor a rendszer az aktuális API-verzióból olvassa be a házirendet.</span><span class="sxs-lookup"><span data-stu-id="29864-127">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="29864-128">-Környezet</span><span class="sxs-lookup"><span data-stu-id="29864-128">-Context</span></span>
<span data-ttu-id="29864-129">A **PsApiManagementContext** példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="29864-129">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="29864-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29864-130">-DefaultProfile</span></span>
<span data-ttu-id="29864-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29864-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29864-132">-Force</span><span class="sxs-lookup"><span data-stu-id="29864-132">-Force</span></span>
<span data-ttu-id="29864-133">ps_force</span><span class="sxs-lookup"><span data-stu-id="29864-133">ps_force</span></span>

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

### <span data-ttu-id="29864-134">Formátumú</span><span class="sxs-lookup"><span data-stu-id="29864-134">-Format</span></span>
<span data-ttu-id="29864-135">Az API-kezelési házirend formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="29864-135">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="29864-136">A paraméter alapértelmezett értéke az "Application/vnd. MS-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="29864-136">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="29864-137">-OperationId</span><span class="sxs-lookup"><span data-stu-id="29864-137">-OperationId</span></span>
<span data-ttu-id="29864-138">A meglévő API-művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="29864-138">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="29864-139">Ha ezt a paramétert a *ApiId* -ban adja meg, a parancsmag a műveleti hatókör házirendjét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="29864-139">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

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

### <span data-ttu-id="29864-140">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="29864-140">-ProductId</span></span>
<span data-ttu-id="29864-141">Egy meglévő szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="29864-141">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="29864-142">Ha ezt a paramétert adja meg, a parancsmag a termékspecifikus házirendet adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="29864-142">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

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

### <span data-ttu-id="29864-143">-Saven</span><span class="sxs-lookup"><span data-stu-id="29864-143">-SaveAs</span></span>
<span data-ttu-id="29864-144">Annak a fájlnak az elérési útját adja meg, ahová menteni szeretné az eredményt.</span><span class="sxs-lookup"><span data-stu-id="29864-144">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="29864-145">Ha nem adja meg ezt a paramétert, az eredmény a folyamat csípése.</span><span class="sxs-lookup"><span data-stu-id="29864-145">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="29864-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29864-146">-Confirm</span></span>
<span data-ttu-id="29864-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29864-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29864-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29864-148">-WhatIf</span></span>
<span data-ttu-id="29864-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="29864-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29864-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29864-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29864-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29864-151">CommonParameters</span></span>
<span data-ttu-id="29864-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29864-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29864-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29864-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29864-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29864-154">INPUTS</span></span>

### <span data-ttu-id="29864-155">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="29864-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="29864-156">System. String</span><span class="sxs-lookup"><span data-stu-id="29864-156">System.String</span></span>

### <span data-ttu-id="29864-157">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="29864-157">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="29864-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29864-158">OUTPUTS</span></span>

### <span data-ttu-id="29864-159">System. String</span><span class="sxs-lookup"><span data-stu-id="29864-159">System.String</span></span>

## <span data-ttu-id="29864-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29864-160">NOTES</span></span>

## <span data-ttu-id="29864-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29864-161">RELATED LINKS</span></span>

[<span data-ttu-id="29864-162">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="29864-162">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="29864-163">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="29864-163">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


