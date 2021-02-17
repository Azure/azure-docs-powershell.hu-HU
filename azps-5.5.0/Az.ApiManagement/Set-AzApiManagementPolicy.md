---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
ms.openlocfilehash: ee0a95653dbc949518c485554c6202664d943ba3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210295"
---
# <span data-ttu-id="36139-101">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="36139-101">Set-AzApiManagementPolicy</span></span>

## <span data-ttu-id="36139-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36139-102">SYNOPSIS</span></span>
<span data-ttu-id="36139-103">Beállítja a megadott hatókör-házirendet az API-kezeléshez.</span><span class="sxs-lookup"><span data-stu-id="36139-103">Sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="36139-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="36139-104">SYNTAX</span></span>

### <span data-ttu-id="36139-105">SetTenantLevel (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="36139-105">SetTenantLevel (Default)</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36139-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="36139-106">SetProductLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36139-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="36139-107">SetApiLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36139-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="36139-108">SetOperationLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36139-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="36139-109">DESCRIPTION</span></span>
<span data-ttu-id="36139-110">A **Set-AzApiManagementPolicy parancsmag** beállítja a megadott hatókör-házirendet az API-kezeléshez.</span><span class="sxs-lookup"><span data-stu-id="36139-110">The **Set-AzApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="36139-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="36139-111">EXAMPLES</span></span>

### <span data-ttu-id="36139-112">1. példa: A bérlői szintű házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="36139-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="36139-113">Ez a parancs beállítja a bérlői szintű házirendet egy másik tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="36139-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="36139-114">2. példa: Termékhatókör-házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="36139-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="36139-115">Ez a parancs beállítja az API-kezelés termékhatókörre vonatkozó házirendét.</span><span class="sxs-lookup"><span data-stu-id="36139-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="36139-116">3. példa: API-hatókör házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="36139-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="36139-117">Ez a parancs beállítja az API-hatókör házirendet az API-kezeléshez.</span><span class="sxs-lookup"><span data-stu-id="36139-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="36139-118">4. példa: Művelet-hatókör házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="36139-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="36139-119">Ez a parancs beállítja az API-kezelés művelethatókör-házirendét.</span><span class="sxs-lookup"><span data-stu-id="36139-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="36139-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36139-120">PARAMETERS</span></span>

### <span data-ttu-id="36139-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="36139-121">-ApiId</span></span>
<span data-ttu-id="36139-122">A meglévő API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="36139-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="36139-123">Ha ezt a paramétert adja meg, a parancsmag beállítja az API-hatókör házirendet.</span><span class="sxs-lookup"><span data-stu-id="36139-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

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

### <span data-ttu-id="36139-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="36139-124">-ApiRevision</span></span>
<span data-ttu-id="36139-125">Az API-változat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="36139-125">Identifier of API Revision.</span></span> <span data-ttu-id="36139-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="36139-126">This parameter is optional.</span></span> <span data-ttu-id="36139-127">Ha nincs megadva, a házirend frissül az aktuálisan aktív API-változatban.</span><span class="sxs-lookup"><span data-stu-id="36139-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="36139-128">-Környezet</span><span class="sxs-lookup"><span data-stu-id="36139-128">-Context</span></span>
<span data-ttu-id="36139-129">A **PsApiManagementContext példányát adja meg.**</span><span class="sxs-lookup"><span data-stu-id="36139-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="36139-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36139-130">-DefaultProfile</span></span>
<span data-ttu-id="36139-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36139-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36139-132">-Format</span><span class="sxs-lookup"><span data-stu-id="36139-132">-Format</span></span>
<span data-ttu-id="36139-133">A házirend formátumát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="36139-133">Specifies the format of the policy.</span></span> <span data-ttu-id="36139-134">A `application/vnd.ms-azure-apim.policy+xml` házirendben szereplő kifejezéseknek XML-escape-nek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="36139-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="36139-135">Ha xml-escape-t használ, a házirendnek `application/vnd.ms-azure-apim.policy.raw+xml` nem kell  XML-escape-nek lennie.</span><span class="sxs-lookup"><span data-stu-id="36139-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="36139-136">Az alapértelmezett érték `application/vnd.ms-azure-apim.policy+xml` a .</span><span class="sxs-lookup"><span data-stu-id="36139-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="36139-137">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="36139-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="36139-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="36139-138">-OperationId</span></span>
<span data-ttu-id="36139-139">A meglévő művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="36139-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="36139-140">Ha az ApiId érték meg van adva, akkor a művelet-hatókör házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="36139-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="36139-141">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="36139-141">This parameters is required.</span></span>

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

### <span data-ttu-id="36139-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36139-142">-PassThru</span></span>
<span data-ttu-id="36139-143">passthru</span><span class="sxs-lookup"><span data-stu-id="36139-143">passthru</span></span>

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

### <span data-ttu-id="36139-144">-Házirend</span><span class="sxs-lookup"><span data-stu-id="36139-144">-Policy</span></span>
<span data-ttu-id="36139-145">Karakterláncként adja meg a házirend-dokumentumot.</span><span class="sxs-lookup"><span data-stu-id="36139-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="36139-146">Ez a paraméter akkor szükséges, ha a -*PolicyFilePath* nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="36139-146">This parameter is required if the -*PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="36139-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="36139-147">-PolicyFilePath</span></span>
<span data-ttu-id="36139-148">A házirend-dokumentumfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="36139-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="36139-149">Ez a paraméter  akkor szükséges, ha nincs megadva a Házirend paraméter.</span><span class="sxs-lookup"><span data-stu-id="36139-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="36139-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="36139-150">-PolicyUrl</span></span>
<span data-ttu-id="36139-151">Az URL-cím, ahol a házirend-dokumentum található.</span><span class="sxs-lookup"><span data-stu-id="36139-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="36139-152">Ez a paraméter akkor szükséges, ha nincs megadva a -Policy vagy a -PolicyFilePath.</span><span class="sxs-lookup"><span data-stu-id="36139-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="36139-153">-ProductId</span><span class="sxs-lookup"><span data-stu-id="36139-153">-ProductId</span></span>
<span data-ttu-id="36139-154">A meglévő termék azonosítója.</span><span class="sxs-lookup"><span data-stu-id="36139-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="36139-155">Ha ez a paraméter meg van adva, a parancsmag beállítja a termék-hatókör házirendet.</span><span class="sxs-lookup"><span data-stu-id="36139-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

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

### <span data-ttu-id="36139-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36139-156">CommonParameters</span></span>
<span data-ttu-id="36139-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36139-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36139-158">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36139-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36139-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36139-159">INPUTS</span></span>

### <span data-ttu-id="36139-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="36139-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="36139-161">System.String</span><span class="sxs-lookup"><span data-stu-id="36139-161">System.String</span></span>

### <span data-ttu-id="36139-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="36139-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="36139-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36139-163">OUTPUTS</span></span>

### <span data-ttu-id="36139-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="36139-164">System.Boolean</span></span>

## <span data-ttu-id="36139-165">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="36139-165">NOTES</span></span>

## <span data-ttu-id="36139-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36139-166">RELATED LINKS</span></span>

[<span data-ttu-id="36139-167">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="36139-167">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="36139-168">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="36139-168">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)


