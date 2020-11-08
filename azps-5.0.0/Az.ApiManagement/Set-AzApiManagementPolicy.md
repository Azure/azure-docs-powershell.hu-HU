---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
ms.openlocfilehash: ee0a95653dbc949518c485554c6202664d943ba3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195432"
---
# <span data-ttu-id="92799-101">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="92799-101">Set-AzApiManagementPolicy</span></span>

## <span data-ttu-id="92799-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92799-102">SYNOPSIS</span></span>
<span data-ttu-id="92799-103">Az API-kezeléshez megadott hatóköri házirend beállítása.</span><span class="sxs-lookup"><span data-stu-id="92799-103">Sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="92799-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92799-104">SYNTAX</span></span>

### <span data-ttu-id="92799-105">SetTenantLevel (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="92799-105">SetTenantLevel (Default)</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92799-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="92799-106">SetProductLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92799-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="92799-107">SetApiLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92799-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="92799-108">SetOperationLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92799-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="92799-109">DESCRIPTION</span></span>
<span data-ttu-id="92799-110">A **set-AzApiManagementPolicy** PARANCSMAG az API-kezeléshez megadott hatóköri házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="92799-110">The **Set-AzApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="92799-111">Példák</span><span class="sxs-lookup"><span data-stu-id="92799-111">EXAMPLES</span></span>

### <span data-ttu-id="92799-112">Példa 1: a bérlői szint házirendjének beállítása</span><span class="sxs-lookup"><span data-stu-id="92799-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="92799-113">Ez a parancs a bérlői szintű házirendet egy tenantpolicy.xml nevű fájlból állítja be.</span><span class="sxs-lookup"><span data-stu-id="92799-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="92799-114">2. példa: termékspecifikus házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="92799-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="92799-115">Ez a parancs az API-kezeléshez tartozó termékspecifikus házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="92799-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="92799-116">3. példa: API-scope-házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="92799-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="92799-117">Ez a parancs az API-menedzsment API-hatóköri házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="92799-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="92799-118">4. példa: a műveleti tartomány házirendjének beállítása</span><span class="sxs-lookup"><span data-stu-id="92799-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="92799-119">Ez a parancs beállítja az API-kezeléshez szükséges műveleti hatóköri házirendet.</span><span class="sxs-lookup"><span data-stu-id="92799-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="92799-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92799-120">PARAMETERS</span></span>

### <span data-ttu-id="92799-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="92799-121">-ApiId</span></span>
<span data-ttu-id="92799-122">A meglévő API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="92799-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="92799-123">Ha ezt a paramétert adja meg, a parancsmag az API-scope házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="92799-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

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

### <span data-ttu-id="92799-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="92799-124">-ApiRevision</span></span>
<span data-ttu-id="92799-125">Az API-módosítás azonosítója</span><span class="sxs-lookup"><span data-stu-id="92799-125">Identifier of API Revision.</span></span> <span data-ttu-id="92799-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="92799-126">This parameter is optional.</span></span> <span data-ttu-id="92799-127">Ha nem adja meg, a program frissíti a házirendet a jelenleg aktív API-verzióban.</span><span class="sxs-lookup"><span data-stu-id="92799-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="92799-128">-Környezet</span><span class="sxs-lookup"><span data-stu-id="92799-128">-Context</span></span>
<span data-ttu-id="92799-129">A **PsApiManagementContext** példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="92799-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="92799-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92799-130">-DefaultProfile</span></span>
<span data-ttu-id="92799-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92799-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92799-132">Formátumú</span><span class="sxs-lookup"><span data-stu-id="92799-132">-Format</span></span>
<span data-ttu-id="92799-133">A házirend formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="92799-133">Specifies the format of the policy.</span></span> <span data-ttu-id="92799-134">Használatakor `application/vnd.ms-azure-apim.policy+xml` a házirendben található kifejezéseknek XML-escapenak kell lenniük.</span><span class="sxs-lookup"><span data-stu-id="92799-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="92799-135">Ha `application/vnd.ms-azure-apim.policy.raw+xml` **nem** szükséges, hogy a házirend XML-megmeneküljon.</span><span class="sxs-lookup"><span data-stu-id="92799-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="92799-136">Az alapértelmezett érték `application/vnd.ms-azure-apim.policy+xml` .</span><span class="sxs-lookup"><span data-stu-id="92799-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="92799-137">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="92799-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="92799-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="92799-138">-OperationId</span></span>
<span data-ttu-id="92799-139">A meglévő művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="92799-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="92799-140">Ha a ApiId megadásakor a művelet hatóköre házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="92799-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="92799-141">Ehhez a paraméterekre van szükség.</span><span class="sxs-lookup"><span data-stu-id="92799-141">This parameters is required.</span></span>

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

### <span data-ttu-id="92799-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92799-142">-PassThru</span></span>
<span data-ttu-id="92799-143">passthru</span><span class="sxs-lookup"><span data-stu-id="92799-143">passthru</span></span>

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

### <span data-ttu-id="92799-144">-Házirend</span><span class="sxs-lookup"><span data-stu-id="92799-144">-Policy</span></span>
<span data-ttu-id="92799-145">A házirend-dokumentumot karakterláncként adja meg.</span><span class="sxs-lookup"><span data-stu-id="92799-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="92799-146">Ez a paraméter akkor szükséges, ha a- *PolicyFilePath* nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="92799-146">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="92799-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="92799-147">-PolicyFilePath</span></span>
<span data-ttu-id="92799-148">A házirendfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="92799-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="92799-149">Ez a paraméter akkor szükséges, ha a *házirend* paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="92799-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="92799-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="92799-150">-PolicyUrl</span></span>
<span data-ttu-id="92799-151">Az URL-cím, ahol a házirend-dokumentumot tárolják.</span><span class="sxs-lookup"><span data-stu-id="92799-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="92799-152">Ezt a paramétert akkor kötelező megadni, ha a házirend-vagy PolicyFilePath nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="92799-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="92799-153">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="92799-153">-ProductId</span></span>
<span data-ttu-id="92799-154">A meglévő szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="92799-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="92799-155">Ha ezt a paramétert adja meg, a parancsmag a termékspecifikus házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="92799-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

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

### <span data-ttu-id="92799-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92799-156">CommonParameters</span></span>
<span data-ttu-id="92799-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92799-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92799-158">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="92799-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92799-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92799-159">INPUTS</span></span>

### <span data-ttu-id="92799-160">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="92799-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="92799-161">System. String</span><span class="sxs-lookup"><span data-stu-id="92799-161">System.String</span></span>

### <span data-ttu-id="92799-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="92799-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="92799-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92799-163">OUTPUTS</span></span>

### <span data-ttu-id="92799-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="92799-164">System.Boolean</span></span>

## <span data-ttu-id="92799-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92799-165">NOTES</span></span>

## <span data-ttu-id="92799-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92799-166">RELATED LINKS</span></span>

[<span data-ttu-id="92799-167">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="92799-167">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="92799-168">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="92799-168">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)

