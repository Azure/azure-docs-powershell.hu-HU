---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: b5690dfc1d85483b10fc7cd08606c4555784e8e0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398733"
---
# <span data-ttu-id="4ab95-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4ab95-101">Get-AzADUser</span></span>

## <span data-ttu-id="4ab95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ab95-102">SYNOPSIS</span></span>
<span data-ttu-id="4ab95-103">Szűri az active directory-felhasználókat.</span><span class="sxs-lookup"><span data-stu-id="4ab95-103">Filters active directory users.</span></span>

## <span data-ttu-id="4ab95-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4ab95-104">SYNTAX</span></span>

### <span data-ttu-id="4ab95-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4ab95-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4ab95-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ab95-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4ab95-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ab95-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4ab95-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ab95-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4ab95-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ab95-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4ab95-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ab95-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="4ab95-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4ab95-111">DESCRIPTION</span></span>
<span data-ttu-id="4ab95-112">Szűri az active directory-felhasználókat.</span><span class="sxs-lookup"><span data-stu-id="4ab95-112">Filters active directory users.</span></span>

## <span data-ttu-id="4ab95-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4ab95-113">EXAMPLES</span></span>

### <span data-ttu-id="4ab95-114">1. példa – Az összes felhasználó felsorolása</span><span class="sxs-lookup"><span data-stu-id="4ab95-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="4ab95-115">Egy bérlő összes AD-felhasználóját felsorolja.</span><span class="sxs-lookup"><span data-stu-id="4ab95-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="4ab95-116">2. példa: Az összes felhasználó felsorolása lapozás használatával</span><span class="sxs-lookup"><span data-stu-id="4ab95-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="4ab95-117">A bérlői webhely első 100 AD-felhasználóját sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="4ab95-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="4ab95-118">3. példa: Az AD-felhasználó lekérte egyszerű felhasználónév alapján</span><span class="sxs-lookup"><span data-stu-id="4ab95-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="4ab95-119">Az AD-felhasználót a következő felhasználónévvel kapja meg: " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="4ab95-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="4ab95-120">4. példa – Lista keresési karakterlánc alapján</span><span class="sxs-lookup"><span data-stu-id="4ab95-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="4ab95-121">Azokat az AD-felhasználókat sorolja fel, akiknek a megjelenítendő neve "József" névvel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="4ab95-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="4ab95-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ab95-122">PARAMETERS</span></span>

### <span data-ttu-id="4ab95-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ab95-123">-DefaultProfile</span></span>
<span data-ttu-id="4ab95-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4ab95-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ab95-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4ab95-125">-DisplayName</span></span>
<span data-ttu-id="4ab95-126">A felhasználó megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="4ab95-126">The display name of the user.</span></span>

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

### <span data-ttu-id="4ab95-127">-First</span><span class="sxs-lookup"><span data-stu-id="4ab95-127">-First</span></span>
<span data-ttu-id="4ab95-128">A vissza nem térhet objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="4ab95-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="4ab95-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="4ab95-129">-IncludeTotalCount</span></span>
<span data-ttu-id="4ab95-130">Az adatkészletben lévő objektumok számát jelenti.</span><span class="sxs-lookup"><span data-stu-id="4ab95-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="4ab95-131">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="4ab95-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="4ab95-132">-Mail</span><span class="sxs-lookup"><span data-stu-id="4ab95-132">-Mail</span></span>
<span data-ttu-id="4ab95-133">A felhasználói e-mail.</span><span class="sxs-lookup"><span data-stu-id="4ab95-133">The user mail.</span></span>

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

### <span data-ttu-id="4ab95-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4ab95-134">-ObjectId</span></span>
<span data-ttu-id="4ab95-135">A felhasználó objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="4ab95-135">Object id of the user.</span></span>

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

### <span data-ttu-id="4ab95-136">-Skip</span><span class="sxs-lookup"><span data-stu-id="4ab95-136">-Skip</span></span>
<span data-ttu-id="4ab95-137">Figyelmen kívül hagyja az első N objektumot, majd beveszi a fennmaradó objektumokat.</span><span class="sxs-lookup"><span data-stu-id="4ab95-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="4ab95-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="4ab95-138">-StartsWith</span></span>
<span data-ttu-id="4ab95-139">Segítségével megkeresheti a megadott karakterláncot használó felhasználókat.</span><span class="sxs-lookup"><span data-stu-id="4ab95-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="4ab95-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="4ab95-140">-UserPrincipalName</span></span>
<span data-ttu-id="4ab95-141">A felhasználó upn-ját.</span><span class="sxs-lookup"><span data-stu-id="4ab95-141">UPN of the user.</span></span>

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

### <span data-ttu-id="4ab95-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ab95-142">CommonParameters</span></span>
<span data-ttu-id="4ab95-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ab95-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ab95-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ab95-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ab95-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ab95-145">INPUTS</span></span>

### <span data-ttu-id="4ab95-146">System.String</span><span class="sxs-lookup"><span data-stu-id="4ab95-146">System.String</span></span>

### <span data-ttu-id="4ab95-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="4ab95-147">System.Guid</span></span>

## <span data-ttu-id="4ab95-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ab95-148">OUTPUTS</span></span>

### <span data-ttu-id="4ab95-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="4ab95-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="4ab95-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4ab95-150">NOTES</span></span>

## <span data-ttu-id="4ab95-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ab95-151">RELATED LINKS</span></span>

[<span data-ttu-id="4ab95-152">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4ab95-152">New-AzADUser</span></span>](./New-AzADUser.md)


[<span data-ttu-id="4ab95-153">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4ab95-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

