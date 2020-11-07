---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: b19571025aeb6349277e9ae366146774862e8a80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672585"
---
# <span data-ttu-id="ebb43-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ebb43-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="ebb43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ebb43-102">SYNOPSIS</span></span>
<span data-ttu-id="ebb43-103">Szűri az Active Directory felhasználóit.</span><span class="sxs-lookup"><span data-stu-id="ebb43-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebb43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ebb43-104">SYNTAX</span></span>

### <span data-ttu-id="ebb43-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ebb43-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ebb43-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebb43-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ebb43-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebb43-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ebb43-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebb43-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ebb43-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebb43-109">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ebb43-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebb43-110">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="ebb43-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="ebb43-111">DESCRIPTION</span></span>
<span data-ttu-id="ebb43-112">Szűri az Active Directory felhasználóit.</span><span class="sxs-lookup"><span data-stu-id="ebb43-112">Filters active directory users.</span></span>

## <span data-ttu-id="ebb43-113">Példák</span><span class="sxs-lookup"><span data-stu-id="ebb43-113">EXAMPLES</span></span>

### <span data-ttu-id="ebb43-114">Példa 1 – minden felhasználó listázása</span><span class="sxs-lookup"><span data-stu-id="ebb43-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="ebb43-115">Felsorolja a bérlői fiók összes felhasználóját.</span><span class="sxs-lookup"><span data-stu-id="ebb43-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="ebb43-116">Példa 2 – a lapozófájlt használó összes felhasználó listázása</span><span class="sxs-lookup"><span data-stu-id="ebb43-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzureRmADUser -First 100
```

<span data-ttu-id="ebb43-117">Felsorolja az első 100 AD-felhasználókat a bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="ebb43-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="ebb43-118">Példa 3 – az AD-felhasználó beolvasása a felhasználó egyszerű nevében</span><span class="sxs-lookup"><span data-stu-id="ebb43-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzureRmADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="ebb43-119">Beolvassa a felhasználó egyszerű felhasználónevét " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="ebb43-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="ebb43-120">Példa 4 – keresés karakterlánc szerinti felsorolás</span><span class="sxs-lookup"><span data-stu-id="ebb43-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="ebb43-121">Felsorolja azokat az AD-felhasználókat, akiknek a megjelenítendő neve "Joe"-val kezdődik.</span><span class="sxs-lookup"><span data-stu-id="ebb43-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="ebb43-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ebb43-122">PARAMETERS</span></span>

### <span data-ttu-id="ebb43-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebb43-123">-DefaultProfile</span></span>
<span data-ttu-id="ebb43-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ebb43-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ebb43-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ebb43-125">-DisplayName</span></span>
<span data-ttu-id="ebb43-126">A felhasználó megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="ebb43-126">The display name of the user.</span></span>

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

### <span data-ttu-id="ebb43-127">– Első</span><span class="sxs-lookup"><span data-stu-id="ebb43-127">-First</span></span>
<span data-ttu-id="ebb43-128">A visszaadni kívánt objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="ebb43-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="ebb43-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="ebb43-129">-IncludeTotalCount</span></span>
<span data-ttu-id="ebb43-130">Az adathalmaz objektumainak számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="ebb43-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="ebb43-131">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="ebb43-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="ebb43-132">-Mail</span><span class="sxs-lookup"><span data-stu-id="ebb43-132">-Mail</span></span>
<span data-ttu-id="ebb43-133">A felhasználó e-mail-címe.</span><span class="sxs-lookup"><span data-stu-id="ebb43-133">The user mail.</span></span>

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

### <span data-ttu-id="ebb43-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ebb43-134">-ObjectId</span></span>
<span data-ttu-id="ebb43-135">A felhasználó objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ebb43-135">Object id of the user.</span></span>

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

### <span data-ttu-id="ebb43-136">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="ebb43-136">-Skip</span></span>
<span data-ttu-id="ebb43-137">Figyelmen kívül hagyja az első N objektumokat, és a fennmaradó objektumokat kapja.</span><span class="sxs-lookup"><span data-stu-id="ebb43-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="ebb43-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="ebb43-138">-StartsWith</span></span>
<span data-ttu-id="ebb43-139">A megadott karakterlánccal kezdődő felhasználók megkeresésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="ebb43-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="ebb43-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ebb43-140">-UserPrincipalName</span></span>
<span data-ttu-id="ebb43-141">A felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="ebb43-141">UPN of the user.</span></span>

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

### <span data-ttu-id="ebb43-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebb43-142">CommonParameters</span></span>
<span data-ttu-id="ebb43-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ebb43-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebb43-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebb43-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebb43-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebb43-145">INPUTS</span></span>

### <span data-ttu-id="ebb43-146">System. String</span><span class="sxs-lookup"><span data-stu-id="ebb43-146">System.String</span></span>

### <span data-ttu-id="ebb43-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ebb43-147">System.Guid</span></span>

## <span data-ttu-id="ebb43-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebb43-148">OUTPUTS</span></span>

### <span data-ttu-id="ebb43-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="ebb43-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="ebb43-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ebb43-150">NOTES</span></span>

## <span data-ttu-id="ebb43-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ebb43-151">RELATED LINKS</span></span>

[<span data-ttu-id="ebb43-152">Új – AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ebb43-152">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="ebb43-153">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ebb43-153">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="ebb43-154">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ebb43-154">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

