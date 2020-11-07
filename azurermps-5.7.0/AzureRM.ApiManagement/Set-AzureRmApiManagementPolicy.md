---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 0f9ee1c2190dbc3d657ecc52cd85b6af8b0cac4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672660"
---
# <span data-ttu-id="c7799-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c7799-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="c7799-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7799-102">SYNOPSIS</span></span>
<span data-ttu-id="c7799-103">Az API-kezeléshez megadott hatóköri házirend beállítása.</span><span class="sxs-lookup"><span data-stu-id="c7799-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7799-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7799-104">SYNTAX</span></span>

### <span data-ttu-id="c7799-105">SetTenantLevel (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c7799-105">SetTenantLevel (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7799-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="c7799-106">SetProductLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7799-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="c7799-107">SetApiLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7799-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="c7799-108">SetOperationLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7799-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7799-109">DESCRIPTION</span></span>
<span data-ttu-id="c7799-110">A **set-AzureRmApiManagementPolicy** PARANCSMAG az API-kezeléshez megadott hatóköri házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="c7799-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="c7799-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c7799-111">EXAMPLES</span></span>

### <span data-ttu-id="c7799-112">Példa 1: a bérlői szint házirendjének beállítása</span><span class="sxs-lookup"><span data-stu-id="c7799-112">Example 1: Set the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="c7799-113">Ez a parancs a bérlői szintű házirendet egy tenantpolicy.xml nevű fájlból állítja be.</span><span class="sxs-lookup"><span data-stu-id="c7799-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="c7799-114">2. példa: termékspecifikus házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="c7799-114">Example 2: Set a product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="c7799-115">Ez a parancs az API-kezeléshez tartozó termékspecifikus házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="c7799-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="c7799-116">3. példa: API-scope-házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="c7799-116">Example 3: Set API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="c7799-117">Ez a parancs az API-menedzsment API-hatóköri házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="c7799-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="c7799-118">4. példa: a műveleti tartomány házirendjének beállítása</span><span class="sxs-lookup"><span data-stu-id="c7799-118">Example 4: Set operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="c7799-119">Ez a parancs beállítja az API-kezeléshez szükséges műveleti hatóköri házirendet.</span><span class="sxs-lookup"><span data-stu-id="c7799-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="c7799-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7799-120">PARAMETERS</span></span>

### <span data-ttu-id="c7799-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c7799-121">-ApiId</span></span>
<span data-ttu-id="c7799-122">A meglévő API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7799-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="c7799-123">Ha ezt a paramétert adja meg, a parancsmag az API-scope házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="c7799-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7799-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c7799-124">-Context</span></span>
<span data-ttu-id="c7799-125">A **PsApiManagementContext** példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7799-125">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="c7799-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7799-126">-DefaultProfile</span></span>
<span data-ttu-id="c7799-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7799-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="c7799-128">Formátumú</span><span class="sxs-lookup"><span data-stu-id="c7799-128">-Format</span></span>
<span data-ttu-id="c7799-129">A házirend formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7799-129">Specifies the format of the policy.</span></span>
<span data-ttu-id="c7799-130">Az alapértelmezett érték az "Application/vnd. MS-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="c7799-130">The default value is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="c7799-131">-OperationId</span><span class="sxs-lookup"><span data-stu-id="c7799-131">-OperationId</span></span>
<span data-ttu-id="c7799-132">A meglévő művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7799-132">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="c7799-133">Ha a ApiId megadásakor a művelet hatóköre házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7799-133">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="c7799-134">Ehhez a paraméterekre van szükség.</span><span class="sxs-lookup"><span data-stu-id="c7799-134">This parameters is required.</span></span>

```yaml
Type: String
Parameter Sets: SetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7799-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7799-135">-PassThru</span></span>
<span data-ttu-id="c7799-136">passthru</span><span class="sxs-lookup"><span data-stu-id="c7799-136">passthru</span></span>

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

### <span data-ttu-id="c7799-137">-Házirend</span><span class="sxs-lookup"><span data-stu-id="c7799-137">-Policy</span></span>
<span data-ttu-id="c7799-138">A házirend-dokumentumot karakterláncként adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7799-138">Specifies the policy document as a string.</span></span>
<span data-ttu-id="c7799-139">Ez a paraméter akkor szükséges, ha a- *PolicyFilePath* nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="c7799-139">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="c7799-140">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="c7799-140">-PolicyFilePath</span></span>
<span data-ttu-id="c7799-141">A házirendfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7799-141">Specifies the policy document file path.</span></span>
<span data-ttu-id="c7799-142">Ez a paraméter akkor szükséges, ha a *házirend* paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="c7799-142">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="c7799-143">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="c7799-143">-ProductId</span></span>
<span data-ttu-id="c7799-144">A meglévő szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7799-144">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="c7799-145">Ha ezt a paramétert adja meg, a parancsmag a termékspecifikus házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="c7799-145">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: SetProductLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7799-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7799-146">CommonParameters</span></span>
<span data-ttu-id="c7799-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7799-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7799-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7799-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7799-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7799-149">INPUTS</span></span>

### <span data-ttu-id="c7799-150">Nincs</span><span class="sxs-lookup"><span data-stu-id="c7799-150">None</span></span>
<span data-ttu-id="c7799-151">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c7799-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7799-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7799-152">OUTPUTS</span></span>

### <span data-ttu-id="c7799-153">bool</span><span class="sxs-lookup"><span data-stu-id="c7799-153">bool</span></span>

## <span data-ttu-id="c7799-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7799-154">NOTES</span></span>

## <span data-ttu-id="c7799-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7799-155">RELATED LINKS</span></span>

[<span data-ttu-id="c7799-156">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c7799-156">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="c7799-157">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c7799-157">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


