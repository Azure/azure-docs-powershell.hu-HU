---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 75bb963195244a5a1a27ca004eb2795b6b5bb556
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492912"
---
# <span data-ttu-id="e247d-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e247d-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="e247d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e247d-102">SYNOPSIS</span></span>
<span data-ttu-id="e247d-103">Az API-kezeléshez megadott hatóköri házirend beállítása.</span><span class="sxs-lookup"><span data-stu-id="e247d-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e247d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e247d-104">SYNTAX</span></span>

### <span data-ttu-id="e247d-105">SetTenantLevel (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e247d-105">SetTenantLevel (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e247d-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="e247d-106">SetProductLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e247d-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="e247d-107">SetApiLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e247d-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="e247d-108">SetOperationLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e247d-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e247d-109">DESCRIPTION</span></span>
<span data-ttu-id="e247d-110">A **set-AzureRmApiManagementPolicy** PARANCSMAG az API-kezeléshez megadott hatóköri házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="e247d-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="e247d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e247d-111">EXAMPLES</span></span>

### <span data-ttu-id="e247d-112">Példa 1: a bérlői szint házirendjének beállítása</span><span class="sxs-lookup"><span data-stu-id="e247d-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="e247d-113">Ez a parancs a bérlői szintű házirendet egy tenantpolicy.xml nevű fájlból állítja be.</span><span class="sxs-lookup"><span data-stu-id="e247d-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="e247d-114">2. példa: termékspecifikus házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="e247d-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="e247d-115">Ez a parancs az API-kezeléshez tartozó termékspecifikus házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="e247d-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="e247d-116">3. példa: API-scope-házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="e247d-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="e247d-117">Ez a parancs az API-menedzsment API-hatóköri házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="e247d-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="e247d-118">4. példa: a műveleti tartomány házirendjének beállítása</span><span class="sxs-lookup"><span data-stu-id="e247d-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="e247d-119">Ez a parancs beállítja az API-kezeléshez szükséges műveleti hatóköri házirendet.</span><span class="sxs-lookup"><span data-stu-id="e247d-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="e247d-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e247d-120">PARAMETERS</span></span>

### <span data-ttu-id="e247d-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e247d-121">-ApiId</span></span>
<span data-ttu-id="e247d-122">A meglévő API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e247d-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="e247d-123">Ha ezt a paramétert adja meg, a parancsmag az API-scope házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="e247d-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e247d-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="e247d-124">-ApiRevision</span></span>
<span data-ttu-id="e247d-125">Az API-módosítás azonosítója</span><span class="sxs-lookup"><span data-stu-id="e247d-125">Identifier of API Revision.</span></span> <span data-ttu-id="e247d-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="e247d-126">This parameter is optional.</span></span> <span data-ttu-id="e247d-127">Ha nem adja meg, a program frissíti a házirendet a jelenleg aktív API-verzióban.</span><span class="sxs-lookup"><span data-stu-id="e247d-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e247d-128">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e247d-128">-Context</span></span>
<span data-ttu-id="e247d-129">A **PsApiManagementContext** példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e247d-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="e247d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e247d-130">-DefaultProfile</span></span>
<span data-ttu-id="e247d-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e247d-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e247d-132">Formátumú</span><span class="sxs-lookup"><span data-stu-id="e247d-132">-Format</span></span>
<span data-ttu-id="e247d-133">A házirend formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e247d-133">Specifies the format of the policy.</span></span> <span data-ttu-id="e247d-134">Használatakor `application/vnd.ms-azure-apim.policy+xml` a házirendben található kifejezéseknek XML-escapenak kell lenniük.</span><span class="sxs-lookup"><span data-stu-id="e247d-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="e247d-135">Ha `application/vnd.ms-azure-apim.policy.raw+xml` **nem** szükséges, hogy a házirend XML-megmeneküljon.</span><span class="sxs-lookup"><span data-stu-id="e247d-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="e247d-136">Az alapértelmezett érték `application/vnd.ms-azure-apim.policy+xml` .</span><span class="sxs-lookup"><span data-stu-id="e247d-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="e247d-137">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="e247d-137">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: application/vnd.ms-azure-apim.policy.raw+xml, application/vnd.ms-azure-apim.policy+xml

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e247d-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="e247d-138">-OperationId</span></span>
<span data-ttu-id="e247d-139">A meglévő művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e247d-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="e247d-140">Ha a ApiId megadásakor a művelet hatóköre házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="e247d-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="e247d-141">Ehhez a paraméterekre van szükség.</span><span class="sxs-lookup"><span data-stu-id="e247d-141">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e247d-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e247d-142">-PassThru</span></span>
<span data-ttu-id="e247d-143">passthru</span><span class="sxs-lookup"><span data-stu-id="e247d-143">passthru</span></span>

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

### <span data-ttu-id="e247d-144">-Házirend</span><span class="sxs-lookup"><span data-stu-id="e247d-144">-Policy</span></span>
<span data-ttu-id="e247d-145">A házirend-dokumentumot karakterláncként adja meg.</span><span class="sxs-lookup"><span data-stu-id="e247d-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="e247d-146">Ez a paraméter akkor szükséges, ha a- *PolicyFilePath* nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="e247d-146">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="e247d-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="e247d-147">-PolicyFilePath</span></span>
<span data-ttu-id="e247d-148">A házirendfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e247d-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="e247d-149">Ez a paraméter akkor szükséges, ha a *házirend* paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="e247d-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="e247d-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="e247d-150">-PolicyUrl</span></span>
<span data-ttu-id="e247d-151">Az URL-cím, ahol a házirend-dokumentumot tárolják.</span><span class="sxs-lookup"><span data-stu-id="e247d-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="e247d-152">Ezt a paramétert akkor kötelező megadni, ha a házirend-vagy PolicyFilePath nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="e247d-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="e247d-153">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="e247d-153">-ProductId</span></span>
<span data-ttu-id="e247d-154">A meglévő szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e247d-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="e247d-155">Ha ezt a paramétert adja meg, a parancsmag a termékspecifikus házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="e247d-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e247d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e247d-156">CommonParameters</span></span>
<span data-ttu-id="e247d-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e247d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e247d-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e247d-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e247d-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e247d-159">INPUTS</span></span>

### <span data-ttu-id="e247d-160">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e247d-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e247d-161">System. String</span><span class="sxs-lookup"><span data-stu-id="e247d-161">System.String</span></span>

### <span data-ttu-id="e247d-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e247d-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e247d-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e247d-163">OUTPUTS</span></span>

### <span data-ttu-id="e247d-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e247d-164">System.Boolean</span></span>

## <span data-ttu-id="e247d-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e247d-165">NOTES</span></span>

## <span data-ttu-id="e247d-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e247d-166">RELATED LINKS</span></span>

[<span data-ttu-id="e247d-167">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e247d-167">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="e247d-168">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e247d-168">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


