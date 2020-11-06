---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 16eed643397245fa54b2876430042335762ea048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498104"
---
# <span data-ttu-id="59f93-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="59f93-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="59f93-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59f93-102">SYNOPSIS</span></span>
<span data-ttu-id="59f93-103">Megkapja a megadott hatókör-házirendet.</span><span class="sxs-lookup"><span data-stu-id="59f93-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59f93-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59f93-104">SYNTAX</span></span>

### <span data-ttu-id="59f93-105">Bérlői szint (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="59f93-105">Tenant level (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f93-106">Termékek szintje</span><span class="sxs-lookup"><span data-stu-id="59f93-106">Product level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59f93-107">API-szint</span><span class="sxs-lookup"><span data-stu-id="59f93-107">API level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f93-108">Műveleti szint</span><span class="sxs-lookup"><span data-stu-id="59f93-108">Operation level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> -OperationId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59f93-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="59f93-109">DESCRIPTION</span></span>
<span data-ttu-id="59f93-110">A **Get-AzureRmApiManagementPolicy** parancsmag a megadott hatóköri házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="59f93-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="59f93-111">Példák</span><span class="sxs-lookup"><span data-stu-id="59f93-111">EXAMPLES</span></span>

### <span data-ttu-id="59f93-112">Példa 1: a bérlői szint házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="59f93-112">Example 1: Get the tenant level policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="59f93-113">Ez a parancs bérlői szintű házirendet kap, és egy tenantpolicy.xml nevű fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="59f93-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="59f93-114">2. példa: a termékspecifikus házirend beszerzése</span><span class="sxs-lookup"><span data-stu-id="59f93-114">Example 2: Get the product-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="59f93-115">Ez a parancs a Product-scope Policy házirendet kapja meg</span><span class="sxs-lookup"><span data-stu-id="59f93-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="59f93-116">3. példa: az API-hatókörök házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="59f93-116">Example 3: Get the API-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210"
```

<span data-ttu-id="59f93-117">Ez a parancs API-hatóköri házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="59f93-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="59f93-118">Példa 4: a művelet-hatókör házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="59f93-118">Example 4: Get the operation-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="59f93-119">Ez a parancs a művelet hatóköre házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="59f93-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="59f93-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59f93-120">PARAMETERS</span></span>

### <span data-ttu-id="59f93-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="59f93-121">-ApiId</span></span>
<span data-ttu-id="59f93-122">A meglévő API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="59f93-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="59f93-123">Ha ezt a paramétert adja meg, a parancsmag az API-scope házirendet adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="59f93-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: API level, Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59f93-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="59f93-124">-Context</span></span>
<span data-ttu-id="59f93-125">A **PsApiManagementContext** példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="59f93-125">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="59f93-126">-Force</span><span class="sxs-lookup"><span data-stu-id="59f93-126">-Force</span></span>
<span data-ttu-id="59f93-127">ps_force</span><span class="sxs-lookup"><span data-stu-id="59f93-127">ps_force</span></span>

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

### <span data-ttu-id="59f93-128">Formátumú</span><span class="sxs-lookup"><span data-stu-id="59f93-128">-Format</span></span>
<span data-ttu-id="59f93-129">Az API-kezelési házirend formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="59f93-129">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="59f93-130">A paraméter alapértelmezett értéke az "Application/vnd. MS-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="59f93-130">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="59f93-131">-OperationId</span><span class="sxs-lookup"><span data-stu-id="59f93-131">-OperationId</span></span>
<span data-ttu-id="59f93-132">A meglévő API-művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="59f93-132">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="59f93-133">Ha ezt a paramétert a *ApiId* -ban adja meg, a parancsmag a műveleti hatókör házirendjét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="59f93-133">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59f93-134">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="59f93-134">-ProductId</span></span>
<span data-ttu-id="59f93-135">Egy meglévő szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="59f93-135">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="59f93-136">Ha ezt a paramétert adja meg, a parancsmag a termékspecifikus házirendet adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="59f93-136">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Product level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59f93-137">-Saven</span><span class="sxs-lookup"><span data-stu-id="59f93-137">-SaveAs</span></span>
<span data-ttu-id="59f93-138">Annak a fájlnak az elérési útját adja meg, ahová menteni szeretné az eredményt.</span><span class="sxs-lookup"><span data-stu-id="59f93-138">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="59f93-139">Ha nem adja meg ezt a paramétert, az eredmény a folyamat csípése.</span><span class="sxs-lookup"><span data-stu-id="59f93-139">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="59f93-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="59f93-140">-Confirm</span></span>
<span data-ttu-id="59f93-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="59f93-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f93-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59f93-142">-WhatIf</span></span>
<span data-ttu-id="59f93-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="59f93-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59f93-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="59f93-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f93-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59f93-145">-DefaultProfile</span></span>
<span data-ttu-id="59f93-146">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59f93-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59f93-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59f93-147">CommonParameters</span></span>
<span data-ttu-id="59f93-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59f93-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59f93-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59f93-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59f93-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59f93-150">INPUTS</span></span>

## <span data-ttu-id="59f93-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59f93-151">OUTPUTS</span></span>

### <span data-ttu-id="59f93-152">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="59f93-152">String</span></span>

## <span data-ttu-id="59f93-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59f93-153">NOTES</span></span>

## <span data-ttu-id="59f93-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59f93-154">RELATED LINKS</span></span>

[<span data-ttu-id="59f93-155">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="59f93-155">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="59f93-156">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="59f93-156">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


