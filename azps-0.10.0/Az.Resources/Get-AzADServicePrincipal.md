---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: 01f6b6d6ed119945af7d99bac9227c788976cbab
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398699"
---
# <span data-ttu-id="57c67-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="57c67-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="57c67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57c67-102">SYNOPSIS</span></span>
<span data-ttu-id="57c67-103">Szűri az active directory-szolgáltatásban használható egyszerű címtár-rendszereket.</span><span class="sxs-lookup"><span data-stu-id="57c67-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="57c67-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="57c67-104">SYNTAX</span></span>

### <span data-ttu-id="57c67-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="57c67-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="57c67-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="57c67-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="57c67-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="57c67-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="57c67-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57c67-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="57c67-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57c67-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="57c67-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57c67-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="57c67-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="57c67-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="57c67-112">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="57c67-112">DESCRIPTION</span></span>
<span data-ttu-id="57c67-113">Szűri az active directory-szolgáltatásnévben lévő egyszerű címtárat.</span><span class="sxs-lookup"><span data-stu-id="57c67-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="57c67-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="57c67-114">EXAMPLES</span></span>

### <span data-ttu-id="57c67-115">1. példa – Az AD szolgáltatásnévsőinek felsorolása</span><span class="sxs-lookup"><span data-stu-id="57c67-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="57c67-116">A bérlő összes AD szolgáltatásnévvel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="57c67-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="57c67-117">2. példa : Az AD szolgáltatásban használt egyszerű szolgáltatások listájának felsorolása lapozással</span><span class="sxs-lookup"><span data-stu-id="57c67-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="57c67-118">Egy bérlő első 100 AD szolgáltatásának egyszerű felhasználóját sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="57c67-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="57c67-119">3. példa : Egyszerű szolgáltatásnévlista SPN szerint</span><span class="sxs-lookup"><span data-stu-id="57c67-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="57c67-120">Az SPN "36f81fc3-b00f-48cd-8218-3879f51ff39f" szolgáltatásnévvel.</span><span class="sxs-lookup"><span data-stu-id="57c67-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="57c67-121">4. példa : A szolgáltatásnévnév felsorolása keresési karakterlánc alapján</span><span class="sxs-lookup"><span data-stu-id="57c67-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="57c67-122">Felsorolja azokat az AD szolgáltatásneveket, amelyeknek a megjelenítendő neve "Web" kezdetekkel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="57c67-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="57c67-123">5. példa : Egyszerű szolgáltatásnév listázása pipázással</span><span class="sxs-lookup"><span data-stu-id="57c67-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="57c67-124">A (39e64ec6-569b-4030-8e1c-c3c519a05d69) objektumazonosítójú AD alkalmazást, és a Get-AzADServicePrincipal-parancsmagba beömlve felsorolja az adott alkalmazás összes szolgáltatásnévét.</span><span class="sxs-lookup"><span data-stu-id="57c67-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="57c67-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57c67-125">PARAMETERS</span></span>

### <span data-ttu-id="57c67-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="57c67-126">-ApplicationId</span></span>
<span data-ttu-id="57c67-127">Az egyszerű szolgáltatásalkalmazás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="57c67-127">The service principal application id.</span></span>

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

### <span data-ttu-id="57c67-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="57c67-128">-ApplicationObject</span></span>
<span data-ttu-id="57c67-129">Az az alkalmazásobjektum, amelynek a szolgáltatásnév beolvasása folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="57c67-129">The application object whose service principal is being retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57c67-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57c67-130">-DefaultProfile</span></span>
<span data-ttu-id="57c67-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="57c67-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c67-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="57c67-132">-DisplayName</span></span>
<span data-ttu-id="57c67-133">Az egyszerű szolgáltatásnév megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="57c67-133">The service principal display name.</span></span>

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

### <span data-ttu-id="57c67-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="57c67-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="57c67-135">Az egyszerű szolgáltatásnév keresési karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="57c67-135">The service principal search string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c67-136">-First</span><span class="sxs-lookup"><span data-stu-id="57c67-136">-First</span></span>
<span data-ttu-id="57c67-137">A vissza nem térhet objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="57c67-137">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="57c67-138">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="57c67-138">-IncludeTotalCount</span></span>
<span data-ttu-id="57c67-139">Az adatkészletben lévő objektumok számát jelenti.</span><span class="sxs-lookup"><span data-stu-id="57c67-139">Reports the number of objects in the data set.</span></span> <span data-ttu-id="57c67-140">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="57c67-140">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="57c67-141">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="57c67-141">-ObjectId</span></span>
<span data-ttu-id="57c67-142">A szolgáltatásnév objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="57c67-142">Object id of the service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c67-143">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="57c67-143">-ServicePrincipalName</span></span>
<span data-ttu-id="57c67-144">A szolgáltatás SPN-ét.</span><span class="sxs-lookup"><span data-stu-id="57c67-144">SPN of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c67-145">-Skip</span><span class="sxs-lookup"><span data-stu-id="57c67-145">-Skip</span></span>
<span data-ttu-id="57c67-146">Figyelmen kívül hagyja az első N objektumot, majd beveszi a fennmaradó objektumokat.</span><span class="sxs-lookup"><span data-stu-id="57c67-146">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="57c67-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c67-147">CommonParameters</span></span>
<span data-ttu-id="57c67-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57c67-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c67-149">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57c67-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c67-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57c67-150">INPUTS</span></span>

### <span data-ttu-id="57c67-151">System.String</span><span class="sxs-lookup"><span data-stu-id="57c67-151">System.String</span></span>

### <span data-ttu-id="57c67-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="57c67-152">System.Guid</span></span>

### <span data-ttu-id="57c67-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="57c67-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="57c67-154">Paraméterek: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="57c67-154">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="57c67-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57c67-155">OUTPUTS</span></span>

### <span data-ttu-id="57c67-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="57c67-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="57c67-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="57c67-157">NOTES</span></span>

## <span data-ttu-id="57c67-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57c67-158">RELATED LINKS</span></span>

[<span data-ttu-id="57c67-159">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="57c67-159">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)


[<span data-ttu-id="57c67-160">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="57c67-160">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="57c67-161">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="57c67-161">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="57c67-162">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="57c67-162">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

