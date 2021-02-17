---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 545722e48095f8b77104bb6ff24b856bd76e3312
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399719"
---
# <span data-ttu-id="9e020-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="9e020-101">Get-AzADApplication</span></span>

## <span data-ttu-id="9e020-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e020-102">SYNOPSIS</span></span>
<span data-ttu-id="9e020-103">A meglévő Azure Active Directory-alkalmazások listája.</span><span class="sxs-lookup"><span data-stu-id="9e020-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="9e020-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9e020-104">SYNTAX</span></span>

### <span data-ttu-id="9e020-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9e020-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="9e020-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e020-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="9e020-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e020-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="9e020-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e020-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="9e020-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e020-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="9e020-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e020-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="9e020-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9e020-111">DESCRIPTION</span></span>
<span data-ttu-id="9e020-112">A meglévő Azure Active Directory-alkalmazások listája.</span><span class="sxs-lookup"><span data-stu-id="9e020-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="9e020-113">Az alkalmazáskeresést az ObjectId, az ApplicationId, az IdentifierUri vagy a DisplayName segítségével lehet.</span><span class="sxs-lookup"><span data-stu-id="9e020-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="9e020-114">Ha nincs megadva paraméter, akkor a bérlő alatti összes alkalmazást lehívja.</span><span class="sxs-lookup"><span data-stu-id="9e020-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="9e020-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9e020-115">EXAMPLES</span></span>

### <span data-ttu-id="9e020-116">1. példa – Az összes alkalmazás felsorolása</span><span class="sxs-lookup"><span data-stu-id="9e020-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="9e020-117">A bérlői webhely összes alkalmazását felsorolja.</span><span class="sxs-lookup"><span data-stu-id="9e020-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="9e020-118">2. példa: Lapozást használó alkalmazások felsorolása</span><span class="sxs-lookup"><span data-stu-id="9e020-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="9e020-119">A bérlői webhely alatt található első 100 alkalmazás listája.</span><span class="sxs-lookup"><span data-stu-id="9e020-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="9e020-120">3. példa : Alkalmazás lekérte azonosító alapján URI</span><span class="sxs-lookup"><span data-stu-id="9e020-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="9e020-121">Az alkalmazás uri azonosítóját "" "- ként http://mySecretApp1 kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9e020-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="9e020-122">4. példa : Alkalmazás be szerezni objektumazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="9e020-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="9e020-123">A (39e64ec6-569b-4030-8e1c-c3c519a05d69) objektumazonosítót használja.</span><span class="sxs-lookup"><span data-stu-id="9e020-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="9e020-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e020-124">PARAMETERS</span></span>

### <span data-ttu-id="9e020-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9e020-125">-ApplicationId</span></span>
<span data-ttu-id="9e020-126">A lehívni szükséges alkalmazás alkalmazásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="9e020-126">The application id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e020-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e020-127">-DefaultProfile</span></span>
<span data-ttu-id="9e020-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9e020-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e020-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9e020-129">-DisplayName</span></span>
<span data-ttu-id="9e020-130">Az alkalmazás megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="9e020-130">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e020-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="9e020-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="9e020-132">Az összes alkalmazás lehívása a megjelenítendő névvel kezdve.</span><span class="sxs-lookup"><span data-stu-id="9e020-132">Fetch all applications starting with the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e020-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="9e020-133">-IdentifierUri</span></span>
<span data-ttu-id="9e020-134">A lehívni szükséges alkalmazás egyedi azonosítója Uri.</span><span class="sxs-lookup"><span data-stu-id="9e020-134">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e020-135">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9e020-135">-ObjectId</span></span>
<span data-ttu-id="9e020-136">A lehívni szükséges alkalmazás objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="9e020-136">The object id of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e020-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="9e020-137">-IncludeTotalCount</span></span>
<span data-ttu-id="9e020-138">Az adatkészletben lévő objektumok számát jelenti.</span><span class="sxs-lookup"><span data-stu-id="9e020-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="9e020-139">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="9e020-139">Currently, this parameter does nothing.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e020-140">-Skip</span><span class="sxs-lookup"><span data-stu-id="9e020-140">-Skip</span></span>
<span data-ttu-id="9e020-141">Figyelmen kívül hagyja az első N objektumot, majd beveszi a fennmaradó objektumokat.</span><span class="sxs-lookup"><span data-stu-id="9e020-141">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e020-142">-First</span><span class="sxs-lookup"><span data-stu-id="9e020-142">-First</span></span>
<span data-ttu-id="9e020-143">A vissza nem térhet objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="9e020-143">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e020-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e020-144">CommonParameters</span></span>
<span data-ttu-id="9e020-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e020-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e020-146">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e020-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e020-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e020-147">INPUTS</span></span>

### <span data-ttu-id="9e020-148">System.String</span><span class="sxs-lookup"><span data-stu-id="9e020-148">System.String</span></span>

### <span data-ttu-id="9e020-149">System.Guid</span><span class="sxs-lookup"><span data-stu-id="9e020-149">System.Guid</span></span>

## <span data-ttu-id="9e020-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e020-150">OUTPUTS</span></span>

### <span data-ttu-id="9e020-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="9e020-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="9e020-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9e020-152">NOTES</span></span>

## <span data-ttu-id="9e020-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e020-153">RELATED LINKS</span></span>

[<span data-ttu-id="9e020-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="9e020-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="9e020-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="9e020-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="9e020-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="9e020-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="9e020-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="9e020-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)


[<span data-ttu-id="9e020-158">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="9e020-158">New-AzADApplication</span></span>](./New-AzADApplication.md)

