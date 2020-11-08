---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 884d5086c8966da8622d48e85f5f4b3009fcc94f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188207"
---
# <span data-ttu-id="ffbb4-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ffbb4-101">Get-AzADUser</span></span>

## <span data-ttu-id="ffbb4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ffbb4-102">SYNOPSIS</span></span>
<span data-ttu-id="ffbb4-103">Szűri az Active Directory felhasználóit.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-103">Filters active directory users.</span></span>

## <span data-ttu-id="ffbb4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ffbb4-104">SYNTAX</span></span>

### <span data-ttu-id="ffbb4-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ffbb4-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ffbb4-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffbb4-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ffbb4-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffbb4-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ffbb4-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffbb4-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ffbb4-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffbb4-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ffbb4-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffbb4-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="ffbb4-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="ffbb4-111">DESCRIPTION</span></span>
<span data-ttu-id="ffbb4-112">Szűri az Active Directory felhasználóit.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-112">Filters active directory users.</span></span>

## <span data-ttu-id="ffbb4-113">Példák</span><span class="sxs-lookup"><span data-stu-id="ffbb4-113">EXAMPLES</span></span>

### <span data-ttu-id="ffbb4-114">Példa 1: az összes felhasználó listázása</span><span class="sxs-lookup"><span data-stu-id="ffbb4-114">Example 1: List all users</span></span>

```powershell
PS C:\> Get-AzADUser
```

<span data-ttu-id="ffbb4-115">Felsorolja a bérlői fiók összes felhasználóját.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="ffbb4-116">2. példa: a lapozófájlokat használó összes felhasználó listázása</span><span class="sxs-lookup"><span data-stu-id="ffbb4-116">Example 2: List all users using paging</span></span>

```powershell
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="ffbb4-117">Felsorolja az első 100 AD-felhasználókat a bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="ffbb4-118">3. példa: az AD-felhasználó beolvasása egyszerű felhasználónévvel</span><span class="sxs-lookup"><span data-stu-id="ffbb4-118">Example 3: Get AD user by user principal name</span></span>

```powershell
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="ffbb4-119">Beolvassa a felhasználó egyszerű felhasználónevét " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="ffbb4-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="ffbb4-120">Példa 4: lista keresési karakterlánc szerint</span><span class="sxs-lookup"><span data-stu-id="ffbb4-120">Example 4: List by search string</span></span>

```powershell
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="ffbb4-121">Felsorolja azokat az AD-felhasználókat, akiknek a megjelenítendő neve "Joe"-val kezdődik.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="ffbb4-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ffbb4-122">PARAMETERS</span></span>

### <span data-ttu-id="ffbb4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffbb4-123">-DefaultProfile</span></span>
<span data-ttu-id="ffbb4-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ffbb4-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffbb4-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ffbb4-125">-DisplayName</span></span>
<span data-ttu-id="ffbb4-126">A felhasználó megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-126">The display name of the user.</span></span>

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

### <span data-ttu-id="ffbb4-127">-Mail</span><span class="sxs-lookup"><span data-stu-id="ffbb4-127">-Mail</span></span>
<span data-ttu-id="ffbb4-128">A felhasználó e-mail-címe.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-128">The user mail.</span></span>

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

### <span data-ttu-id="ffbb4-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ffbb4-129">-ObjectId</span></span>
<span data-ttu-id="ffbb4-130">A felhasználó objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-130">Object id of the user.</span></span>

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

### <span data-ttu-id="ffbb4-131">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="ffbb4-131">-StartsWith</span></span>
<span data-ttu-id="ffbb4-132">A megadott karakterlánccal kezdődő felhasználók megkeresésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-132">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="ffbb4-133">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ffbb4-133">-UserPrincipalName</span></span>
<span data-ttu-id="ffbb4-134">A felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-134">UPN of the user.</span></span>

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

### <span data-ttu-id="ffbb4-135">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="ffbb4-135">-IncludeTotalCount</span></span>
<span data-ttu-id="ffbb4-136">Az adathalmaz objektumainak számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-136">Reports the number of objects in the data set.</span></span> <span data-ttu-id="ffbb4-137">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-137">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="ffbb4-138">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="ffbb4-138">-Skip</span></span>
<span data-ttu-id="ffbb4-139">Figyelmen kívül hagyja az első N objektumokat, és a fennmaradó objektumokat kapja.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-139">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="ffbb4-140">– Első</span><span class="sxs-lookup"><span data-stu-id="ffbb4-140">-First</span></span>
<span data-ttu-id="ffbb4-141">A visszaadni kívánt objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-141">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="ffbb4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffbb4-142">CommonParameters</span></span>
<span data-ttu-id="ffbb4-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ffbb4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffbb4-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffbb4-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffbb4-145">INPUTS</span></span>

### <span data-ttu-id="ffbb4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="ffbb4-146">System.String</span></span>

## <span data-ttu-id="ffbb4-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffbb4-147">OUTPUTS</span></span>

### <span data-ttu-id="ffbb4-148">Microsoft. Azure. Command. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="ffbb4-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="ffbb4-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ffbb4-149">NOTES</span></span>

## <span data-ttu-id="ffbb4-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ffbb4-150">RELATED LINKS</span></span>

[<span data-ttu-id="ffbb4-151">Új – AzADUser</span><span class="sxs-lookup"><span data-stu-id="ffbb4-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="ffbb4-152">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ffbb4-152">Update-AzADUser</span></span>](./Update-AzADUser.md)

[<span data-ttu-id="ffbb4-153">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ffbb4-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

