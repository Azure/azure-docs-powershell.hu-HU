---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 8073df3946f5bf42ee8b0e5f2c7ae7881e905eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498019"
---
# <span data-ttu-id="95c0a-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="95c0a-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="95c0a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="95c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="95c0a-103">Az API-kezeléshez megadott hatóköri házirend beállítása.</span><span class="sxs-lookup"><span data-stu-id="95c0a-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95c0a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="95c0a-104">SYNTAX</span></span>

### <span data-ttu-id="95c0a-105">Bérlői szint (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="95c0a-105">Tenant level (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95c0a-106">Termékek szintje</span><span class="sxs-lookup"><span data-stu-id="95c0a-106">Product level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95c0a-107">API-szint</span><span class="sxs-lookup"><span data-stu-id="95c0a-107">API level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95c0a-108">Műveleti szint</span><span class="sxs-lookup"><span data-stu-id="95c0a-108">Operation level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95c0a-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="95c0a-109">DESCRIPTION</span></span>
<span data-ttu-id="95c0a-110">A **set-AzureRmApiManagementPolicy** PARANCSMAG az API-kezeléshez megadott hatóköri házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="95c0a-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="95c0a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="95c0a-111">EXAMPLES</span></span>

### <span data-ttu-id="95c0a-112">Példa 1: a bérlői szint házirendjének beállítása</span><span class="sxs-lookup"><span data-stu-id="95c0a-112">Example 1: Set the tenant level policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="95c0a-113">Ez a parancs a bérlői szintű házirendet egy tenantpolicy.xml nevű fájlból állítja be.</span><span class="sxs-lookup"><span data-stu-id="95c0a-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="95c0a-114">2. példa: termékspecifikus házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="95c0a-114">Example 2: Set a product-scope policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="95c0a-115">Ez a parancs az API-kezeléshez tartozó termékspecifikus házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="95c0a-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="95c0a-116">3. példa: API-scope-házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="95c0a-116">Example 3: Set API-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="95c0a-117">Ez a parancs az API-menedzsment API-hatóköri házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="95c0a-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="95c0a-118">4. példa: a műveleti tartomány házirendjének beállítása</span><span class="sxs-lookup"><span data-stu-id="95c0a-118">Example 4: Set operation-scope policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="95c0a-119">Ez a parancs beállítja az API-kezeléshez szükséges műveleti hatóköri házirendet.</span><span class="sxs-lookup"><span data-stu-id="95c0a-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="95c0a-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="95c0a-120">PARAMETERS</span></span>

### <span data-ttu-id="95c0a-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="95c0a-121">-ApiId</span></span>
<span data-ttu-id="95c0a-122">A meglévő API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="95c0a-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="95c0a-123">Ha ezt a paramétert adja meg, a parancsmag az API-scope házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="95c0a-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

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

### <span data-ttu-id="95c0a-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="95c0a-124">-Context</span></span>
<span data-ttu-id="95c0a-125">A **PsApiManagementContext** példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="95c0a-125">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="95c0a-126">Formátumú</span><span class="sxs-lookup"><span data-stu-id="95c0a-126">-Format</span></span>
<span data-ttu-id="95c0a-127">A házirend formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="95c0a-127">Specifies the format of the policy.</span></span>
<span data-ttu-id="95c0a-128">Az alapértelmezett érték az "Application/vnd. MS-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="95c0a-128">The default value is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="95c0a-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="95c0a-129">-OperationId</span></span>
<span data-ttu-id="95c0a-130">A meglévő művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="95c0a-130">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="95c0a-131">Ha a ApiId megadásakor a művelet hatóköre házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="95c0a-131">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="95c0a-132">Ehhez a paraméterekre van szükség.</span><span class="sxs-lookup"><span data-stu-id="95c0a-132">This parameters is required.</span></span>

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

### <span data-ttu-id="95c0a-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95c0a-133">-PassThru</span></span>
<span data-ttu-id="95c0a-134">passthru</span><span class="sxs-lookup"><span data-stu-id="95c0a-134">passthru</span></span>

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

### <span data-ttu-id="95c0a-135">-Házirend</span><span class="sxs-lookup"><span data-stu-id="95c0a-135">-Policy</span></span>
<span data-ttu-id="95c0a-136">A házirend-dokumentumot karakterláncként adja meg.</span><span class="sxs-lookup"><span data-stu-id="95c0a-136">Specifies the policy document as a string.</span></span>
<span data-ttu-id="95c0a-137">Ez a paraméter akkor szükséges, ha a- *PolicyFilePath* nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="95c0a-137">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="95c0a-138">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="95c0a-138">-PolicyFilePath</span></span>
<span data-ttu-id="95c0a-139">A házirendfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="95c0a-139">Specifies the policy document file path.</span></span>
<span data-ttu-id="95c0a-140">Ez a paraméter akkor szükséges, ha a *házirend* paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="95c0a-140">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="95c0a-141">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="95c0a-141">-ProductId</span></span>
<span data-ttu-id="95c0a-142">A meglévő szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="95c0a-142">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="95c0a-143">Ha ezt a paramétert adja meg, a parancsmag a termékspecifikus házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="95c0a-143">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

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

### <span data-ttu-id="95c0a-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95c0a-144">-DefaultProfile</span></span>
<span data-ttu-id="95c0a-145">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="95c0a-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95c0a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95c0a-146">CommonParameters</span></span>
<span data-ttu-id="95c0a-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="95c0a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95c0a-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95c0a-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95c0a-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="95c0a-149">INPUTS</span></span>

## <span data-ttu-id="95c0a-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95c0a-150">OUTPUTS</span></span>

### <span data-ttu-id="95c0a-151">bool</span><span class="sxs-lookup"><span data-stu-id="95c0a-151">bool</span></span>

## <span data-ttu-id="95c0a-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="95c0a-152">NOTES</span></span>

## <span data-ttu-id="95c0a-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95c0a-153">RELATED LINKS</span></span>

[<span data-ttu-id="95c0a-154">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="95c0a-154">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="95c0a-155">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="95c0a-155">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


