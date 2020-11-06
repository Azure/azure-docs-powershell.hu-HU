---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 31b38d07aea51ad1e6bd097cc0c9f7f342e1bfb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495503"
---
# <span data-ttu-id="69a30-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="69a30-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="69a30-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69a30-102">SYNOPSIS</span></span>
<span data-ttu-id="69a30-103">Megkapja a megadott hatókör-házirendet.</span><span class="sxs-lookup"><span data-stu-id="69a30-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69a30-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69a30-104">SYNTAX</span></span>

### <span data-ttu-id="69a30-105">GetTenantLevel (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="69a30-105">GetTenantLevel (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69a30-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="69a30-106">GetProductLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69a30-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="69a30-107">GetApiLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69a30-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="69a30-108">GetOperationLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> -OperationId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69a30-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="69a30-109">DESCRIPTION</span></span>
<span data-ttu-id="69a30-110">A **Get-AzureRmApiManagementPolicy** parancsmag a megadott hatóköri házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="69a30-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="69a30-111">Példák</span><span class="sxs-lookup"><span data-stu-id="69a30-111">EXAMPLES</span></span>

### <span data-ttu-id="69a30-112">Példa 1: a bérlői szint házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="69a30-112">Example 1: Get the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="69a30-113">Ez a parancs bérlői szintű házirendet kap, és egy tenantpolicy.xml nevű fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="69a30-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="69a30-114">2. példa: a termékspecifikus házirend beszerzése</span><span class="sxs-lookup"><span data-stu-id="69a30-114">Example 2: Get the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="69a30-115">Ez a parancs a Product-scope Policy házirendet kapja meg</span><span class="sxs-lookup"><span data-stu-id="69a30-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="69a30-116">3. példa: az API-hatókörök házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="69a30-116">Example 3: Get the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="69a30-117">Ez a parancs API-hatóköri házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="69a30-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="69a30-118">Példa 4: a művelet-hatókör házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="69a30-118">Example 4: Get the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="69a30-119">Ez a parancs a művelet hatóköre házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="69a30-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="69a30-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69a30-120">PARAMETERS</span></span>

### <span data-ttu-id="69a30-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="69a30-121">-ApiId</span></span>
<span data-ttu-id="69a30-122">A meglévő API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="69a30-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="69a30-123">Ha ezt a paramétert adja meg, a parancsmag az API-scope házirendet adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="69a30-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a30-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="69a30-124">-Context</span></span>
<span data-ttu-id="69a30-125">A **PsApiManagementContext** példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="69a30-125">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="69a30-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69a30-126">-DefaultProfile</span></span>
<span data-ttu-id="69a30-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69a30-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="69a30-128">-Force</span><span class="sxs-lookup"><span data-stu-id="69a30-128">-Force</span></span>
<span data-ttu-id="69a30-129">ps_force</span><span class="sxs-lookup"><span data-stu-id="69a30-129">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a30-130">Formátumú</span><span class="sxs-lookup"><span data-stu-id="69a30-130">-Format</span></span>
<span data-ttu-id="69a30-131">Az API-kezelési házirend formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="69a30-131">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="69a30-132">A paraméter alapértelmezett értéke az "Application/vnd. MS-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="69a30-132">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="69a30-133">-OperationId</span><span class="sxs-lookup"><span data-stu-id="69a30-133">-OperationId</span></span>
<span data-ttu-id="69a30-134">A meglévő API-művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="69a30-134">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="69a30-135">Ha ezt a paramétert a *ApiId* -ban adja meg, a parancsmag a műveleti hatókör házirendjét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="69a30-135">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: GetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a30-136">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="69a30-136">-ProductId</span></span>
<span data-ttu-id="69a30-137">Egy meglévő szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="69a30-137">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="69a30-138">Ha ezt a paramétert adja meg, a parancsmag a termékspecifikus házirendet adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="69a30-138">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: GetProductLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a30-139">-Saven</span><span class="sxs-lookup"><span data-stu-id="69a30-139">-SaveAs</span></span>
<span data-ttu-id="69a30-140">Annak a fájlnak az elérési útját adja meg, ahová menteni szeretné az eredményt.</span><span class="sxs-lookup"><span data-stu-id="69a30-140">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="69a30-141">Ha nem adja meg ezt a paramétert, az eredmény a folyamat csípése.</span><span class="sxs-lookup"><span data-stu-id="69a30-141">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="69a30-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="69a30-142">-Confirm</span></span>
<span data-ttu-id="69a30-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="69a30-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a30-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69a30-144">-WhatIf</span></span>
<span data-ttu-id="69a30-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="69a30-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69a30-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69a30-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a30-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69a30-147">CommonParameters</span></span>
<span data-ttu-id="69a30-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69a30-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69a30-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69a30-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69a30-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69a30-150">INPUTS</span></span>

### <span data-ttu-id="69a30-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="69a30-151">None</span></span>
<span data-ttu-id="69a30-152">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="69a30-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="69a30-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69a30-153">OUTPUTS</span></span>

### <span data-ttu-id="69a30-154">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="69a30-154">String</span></span>

## <span data-ttu-id="69a30-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69a30-155">NOTES</span></span>

## <span data-ttu-id="69a30-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69a30-156">RELATED LINKS</span></span>

[<span data-ttu-id="69a30-157">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="69a30-157">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="69a30-158">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="69a30-158">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


