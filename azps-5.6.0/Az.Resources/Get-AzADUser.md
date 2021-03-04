---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 6f5ae29865775368427987dcfc1844c9235db593
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923458"
---
# <span data-ttu-id="d5a9e-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="d5a9e-101">Get-AzADUser</span></span>

## <span data-ttu-id="d5a9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5a9e-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a9e-103">Szűri az Active Directory-felhasználókat.</span><span class="sxs-lookup"><span data-stu-id="d5a9e-103">Filters active directory users.</span></span>

## <span data-ttu-id="d5a9e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d5a9e-104">SYNTAX</span></span>

### <span data-ttu-id="d5a9e-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d5a9e-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d5a9e-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5a9e-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d5a9e-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5a9e-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d5a9e-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5a9e-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d5a9e-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5a9e-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d5a9e-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5a9e-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="d5a9e-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d5a9e-111">DESCRIPTION</span></span>
<span data-ttu-id="d5a9e-112">Szűri az Active Directory-felhasználókat.</span><span class="sxs-lookup"><span data-stu-id="d5a9e-112">Filters active directory users.</span></span>

## <span data-ttu-id="d5a9e-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d5a9e-113">EXAMPLES</span></span>

### <span data-ttu-id="d5a9e-114">1. példa: Az összes felhasználó felsorolása</span><span class="sxs-lookup"><span data-stu-id="d5a9e-114">Example 1: List all users</span></span>

```powershell
PS C:\> Get-AzADUser
```

<span data-ttu-id="d5a9e-115">Egy bérlő összes AD-felhasználóját felsorolja.</span><span class="sxs-lookup"><span data-stu-id="d5a9e-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="d5a9e-116">2. példa: Az összes felhasználó felsorolása lapozás használatával</span><span class="sxs-lookup"><span data-stu-id="d5a9e-116">Example 2: List all users using paging</span></span>

```powershell
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="d5a9e-117">A bérlői webhely első 100 AD-felhasználóját sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="d5a9e-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="d5a9e-118">3. példa: AD-felhasználó lekérte egyszerű felhasználónév alapján</span><span class="sxs-lookup"><span data-stu-id="d5a9e-118">Example 3: Get AD user by user principal name</span></span>

```powershell
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="d5a9e-119">Lekérte az AD-felhasználót egyszerű felhasználónévvel" foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="d5a9e-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="d5a9e-120">4. példa: Lista keresési karakterlánc alapján</span><span class="sxs-lookup"><span data-stu-id="d5a9e-120">Example 4: List by search string</span></span>

```powershell
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="d5a9e-121">Azokat az AD-felhasználókat sorolja fel, akiknek a megjelenítendő neve "József" névvel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="d5a9e-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="d5a9e-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5a9e-122">PARAMETERS</span></span>

### <span data-ttu-id="d5a9e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a9e-123">-DefaultProfile</span></span>
<span data-ttu-id="d5a9e-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d5a9e-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5a9e-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d5a9e-125">-DisplayName</span></span>
<span data-ttu-id="d5a9e-126">A felhasználó megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="d5a9e-126">The display name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a9e-127">-Mail</span><span class="sxs-lookup"><span data-stu-id="d5a9e-127">-Mail</span></span>
<span data-ttu-id="d5a9e-128">A felhasználói e-mail.</span><span class="sxs-lookup"><span data-stu-id="d5a9e-128">The user mail.</span></span>

```yaml
Type: System.String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a9e-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d5a9e-129">-ObjectId</span></span>
<span data-ttu-id="d5a9e-130">A felhasználó objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="d5a9e-130">Object id of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a9e-131">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="d5a9e-131">-StartsWith</span></span>
<span data-ttu-id="d5a9e-132">Segítségével megkeresheti a megadott karakterláncot használó felhasználókat.</span><span class="sxs-lookup"><span data-stu-id="d5a9e-132">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="d5a9e-133">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d5a9e-133">-UserPrincipalName</span></span>
<span data-ttu-id="d5a9e-134">Felhasználó UPN-ét.</span><span class="sxs-lookup"><span data-stu-id="d5a9e-134">UPN of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a9e-135">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="d5a9e-135">-IncludeTotalCount</span></span>
<span data-ttu-id="d5a9e-136">Az adatkészletben lévő objektumok számát jelenti.</span><span class="sxs-lookup"><span data-stu-id="d5a9e-136">Reports the number of objects in the data set.</span></span> <span data-ttu-id="d5a9e-137">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="d5a9e-137">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="d5a9e-138">-Skip</span><span class="sxs-lookup"><span data-stu-id="d5a9e-138">-Skip</span></span>
<span data-ttu-id="d5a9e-139">Figyelmen kívül hagyja az első N objektumot, majd beveszi a fennmaradó objektumokat.</span><span class="sxs-lookup"><span data-stu-id="d5a9e-139">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="d5a9e-140">-First</span><span class="sxs-lookup"><span data-stu-id="d5a9e-140">-First</span></span>
<span data-ttu-id="d5a9e-141">A vissza nem térhet objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="d5a9e-141">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="d5a9e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a9e-142">CommonParameters</span></span>
<span data-ttu-id="d5a9e-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5a9e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a9e-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5a9e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a9e-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5a9e-145">INPUTS</span></span>

### <span data-ttu-id="d5a9e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="d5a9e-146">System.String</span></span>

## <span data-ttu-id="d5a9e-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5a9e-147">OUTPUTS</span></span>

### <span data-ttu-id="d5a9e-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="d5a9e-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="d5a9e-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d5a9e-149">NOTES</span></span>

## <span data-ttu-id="d5a9e-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5a9e-150">RELATED LINKS</span></span>

[<span data-ttu-id="d5a9e-151">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="d5a9e-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="d5a9e-152">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="d5a9e-152">Update-AzADUser</span></span>](./Update-AzADUser.md)

[<span data-ttu-id="d5a9e-153">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="d5a9e-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

