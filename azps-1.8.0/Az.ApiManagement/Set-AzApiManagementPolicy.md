---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
ms.openlocfilehash: 495e076a58d4cb1f19de4f9b7eb740e14aa7b407
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836905"
---
# <span data-ttu-id="566a6-101">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="566a6-101">Set-AzApiManagementPolicy</span></span>

## <span data-ttu-id="566a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="566a6-102">SYNOPSIS</span></span>
<span data-ttu-id="566a6-103">Az API-kezeléshez megadott hatóköri házirend beállítása.</span><span class="sxs-lookup"><span data-stu-id="566a6-103">Sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="566a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="566a6-104">SYNTAX</span></span>

### <span data-ttu-id="566a6-105">SetTenantLevel (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="566a6-105">SetTenantLevel (Default)</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="566a6-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="566a6-106">SetProductLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="566a6-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="566a6-107">SetApiLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="566a6-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="566a6-108">SetOperationLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="566a6-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="566a6-109">DESCRIPTION</span></span>
<span data-ttu-id="566a6-110">A **set-AzApiManagementPolicy** PARANCSMAG az API-kezeléshez megadott hatóköri házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="566a6-110">The **Set-AzApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="566a6-111">Példák</span><span class="sxs-lookup"><span data-stu-id="566a6-111">EXAMPLES</span></span>

### <span data-ttu-id="566a6-112">Példa 1: a bérlői szint házirendjének beállítása</span><span class="sxs-lookup"><span data-stu-id="566a6-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="566a6-113">Ez a parancs a bérlői szintű házirendet egy tenantpolicy.xml nevű fájlból állítja be.</span><span class="sxs-lookup"><span data-stu-id="566a6-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="566a6-114">2. példa: termékspecifikus házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="566a6-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="566a6-115">Ez a parancs az API-kezeléshez tartozó termékspecifikus házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="566a6-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="566a6-116">3. példa: API-scope-házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="566a6-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="566a6-117">Ez a parancs az API-menedzsment API-hatóköri házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="566a6-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="566a6-118">4. példa: a műveleti tartomány házirendjének beállítása</span><span class="sxs-lookup"><span data-stu-id="566a6-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="566a6-119">Ez a parancs beállítja az API-kezeléshez szükséges műveleti hatóköri házirendet.</span><span class="sxs-lookup"><span data-stu-id="566a6-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="566a6-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="566a6-120">PARAMETERS</span></span>

### <span data-ttu-id="566a6-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="566a6-121">-ApiId</span></span>
<span data-ttu-id="566a6-122">A meglévő API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="566a6-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="566a6-123">Ha ezt a paramétert adja meg, a parancsmag az API-scope házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="566a6-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

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

### <span data-ttu-id="566a6-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="566a6-124">-ApiRevision</span></span>
<span data-ttu-id="566a6-125">Az API-módosítás azonosítója</span><span class="sxs-lookup"><span data-stu-id="566a6-125">Identifier of API Revision.</span></span> <span data-ttu-id="566a6-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="566a6-126">This parameter is optional.</span></span> <span data-ttu-id="566a6-127">Ha nem adja meg, a program frissíti a házirendet a jelenleg aktív API-verzióban.</span><span class="sxs-lookup"><span data-stu-id="566a6-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="566a6-128">-Környezet</span><span class="sxs-lookup"><span data-stu-id="566a6-128">-Context</span></span>
<span data-ttu-id="566a6-129">A **PsApiManagementContext** példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="566a6-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="566a6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="566a6-130">-DefaultProfile</span></span>
<span data-ttu-id="566a6-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="566a6-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="566a6-132">Formátumú</span><span class="sxs-lookup"><span data-stu-id="566a6-132">-Format</span></span>
<span data-ttu-id="566a6-133">A házirend formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="566a6-133">Specifies the format of the policy.</span></span> <span data-ttu-id="566a6-134">Használatakor `application/vnd.ms-az-apim.policy+xml` a házirendben található kifejezéseknek XML-escapenak kell lenniük.</span><span class="sxs-lookup"><span data-stu-id="566a6-134">When using `application/vnd.ms-az-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="566a6-135">Ha `application/vnd.ms-az-apim.policy.raw+xml` **nem** szükséges, hogy a házirend XML-megmeneküljon.</span><span class="sxs-lookup"><span data-stu-id="566a6-135">When using `application/vnd.ms-az-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="566a6-136">Az alapértelmezett érték `application/vnd.ms-az-apim.policy+xml` .</span><span class="sxs-lookup"><span data-stu-id="566a6-136">The default value is `application/vnd.ms-az-apim.policy+xml`.</span></span>
<span data-ttu-id="566a6-137">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="566a6-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="566a6-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="566a6-138">-OperationId</span></span>
<span data-ttu-id="566a6-139">A meglévő művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="566a6-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="566a6-140">Ha a ApiId megadásakor a művelet hatóköre házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="566a6-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="566a6-141">Ehhez a paraméterekre van szükség.</span><span class="sxs-lookup"><span data-stu-id="566a6-141">This parameters is required.</span></span>

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

### <span data-ttu-id="566a6-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="566a6-142">-PassThru</span></span>
<span data-ttu-id="566a6-143">passthru</span><span class="sxs-lookup"><span data-stu-id="566a6-143">passthru</span></span>

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

### <span data-ttu-id="566a6-144">-Házirend</span><span class="sxs-lookup"><span data-stu-id="566a6-144">-Policy</span></span>
<span data-ttu-id="566a6-145">A házirend-dokumentumot karakterláncként adja meg.</span><span class="sxs-lookup"><span data-stu-id="566a6-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="566a6-146">Ez a paraméter akkor szükséges, ha a- *PolicyFilePath* nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="566a6-146">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="566a6-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="566a6-147">-PolicyFilePath</span></span>
<span data-ttu-id="566a6-148">A házirendfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="566a6-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="566a6-149">Ez a paraméter akkor szükséges, ha a *házirend* paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="566a6-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="566a6-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="566a6-150">-PolicyUrl</span></span>
<span data-ttu-id="566a6-151">Az URL-cím, ahol a házirend-dokumentumot tárolják.</span><span class="sxs-lookup"><span data-stu-id="566a6-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="566a6-152">Ezt a paramétert akkor kötelező megadni, ha a házirend-vagy PolicyFilePath nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="566a6-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="566a6-153">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="566a6-153">-ProductId</span></span>
<span data-ttu-id="566a6-154">A meglévő szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="566a6-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="566a6-155">Ha ezt a paramétert adja meg, a parancsmag a termékspecifikus házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="566a6-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

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

### <span data-ttu-id="566a6-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="566a6-156">CommonParameters</span></span>
<span data-ttu-id="566a6-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="566a6-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="566a6-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="566a6-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="566a6-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="566a6-159">INPUTS</span></span>

### <span data-ttu-id="566a6-160">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="566a6-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="566a6-161">System. String</span><span class="sxs-lookup"><span data-stu-id="566a6-161">System.String</span></span>

### <span data-ttu-id="566a6-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="566a6-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="566a6-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="566a6-163">OUTPUTS</span></span>

### <span data-ttu-id="566a6-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="566a6-164">System.Boolean</span></span>

## <span data-ttu-id="566a6-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="566a6-165">NOTES</span></span>

## <span data-ttu-id="566a6-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="566a6-166">RELATED LINKS</span></span>

[<span data-ttu-id="566a6-167">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="566a6-167">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="566a6-168">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="566a6-168">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)


