---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
ms.openlocfilehash: 78523d5bef3bfb2461bb524044da14f8aedbbc12
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849537"
---
# <span data-ttu-id="183de-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="183de-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="183de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="183de-102">SYNOPSIS</span></span>
<span data-ttu-id="183de-103">Szűri az Active Directory felhasználóit.</span><span class="sxs-lookup"><span data-stu-id="183de-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="183de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="183de-104">SYNTAX</span></span>

### <span data-ttu-id="183de-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="183de-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="183de-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="183de-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="183de-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="183de-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="183de-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="183de-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="183de-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="183de-109">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="183de-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="183de-110">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="183de-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="183de-111">DESCRIPTION</span></span>
<span data-ttu-id="183de-112">Szűri az Active Directory felhasználóit.</span><span class="sxs-lookup"><span data-stu-id="183de-112">Filters active directory users.</span></span>

## <span data-ttu-id="183de-113">Példák</span><span class="sxs-lookup"><span data-stu-id="183de-113">EXAMPLES</span></span>

### <span data-ttu-id="183de-114">Példa 1 – minden felhasználó listázása</span><span class="sxs-lookup"><span data-stu-id="183de-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="183de-115">Felsorolja a bérlői fiók összes felhasználóját.</span><span class="sxs-lookup"><span data-stu-id="183de-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="183de-116">Példa 2 – a lapozófájlt használó összes felhasználó listázása</span><span class="sxs-lookup"><span data-stu-id="183de-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzureRmADUser -First 100
```

<span data-ttu-id="183de-117">Felsorolja az első 100 AD-felhasználókat a bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="183de-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="183de-118">Példa 3 – az AD-felhasználó beolvasása a felhasználó egyszerű nevében</span><span class="sxs-lookup"><span data-stu-id="183de-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzureRmADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="183de-119">Beolvassa a felhasználó egyszerű felhasználónevét " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="183de-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="183de-120">Példa 4 – keresés karakterlánc szerinti felsorolás</span><span class="sxs-lookup"><span data-stu-id="183de-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="183de-121">Felsorolja azokat az AD-felhasználókat, akiknek a megjelenítendő neve "Joe"-val kezdődik.</span><span class="sxs-lookup"><span data-stu-id="183de-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="183de-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="183de-122">PARAMETERS</span></span>

### <span data-ttu-id="183de-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="183de-123">-DefaultProfile</span></span>
<span data-ttu-id="183de-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="183de-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="183de-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="183de-125">-DisplayName</span></span>
<span data-ttu-id="183de-126">A felhasználó megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="183de-126">The display name of the user.</span></span>

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

### <span data-ttu-id="183de-127">– Első</span><span class="sxs-lookup"><span data-stu-id="183de-127">-First</span></span>
<span data-ttu-id="183de-128">A visszaadni kívánt objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="183de-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="183de-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="183de-129">-IncludeTotalCount</span></span>
<span data-ttu-id="183de-130">Az adathalmaz objektumainak számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="183de-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="183de-131">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="183de-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="183de-132">-Mail</span><span class="sxs-lookup"><span data-stu-id="183de-132">-Mail</span></span>
<span data-ttu-id="183de-133">A felhasználó e-mail-címe.</span><span class="sxs-lookup"><span data-stu-id="183de-133">The user mail.</span></span>

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

### <span data-ttu-id="183de-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="183de-134">-ObjectId</span></span>
<span data-ttu-id="183de-135">A felhasználó objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="183de-135">Object id of the user.</span></span>

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

### <span data-ttu-id="183de-136">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="183de-136">-Skip</span></span>
<span data-ttu-id="183de-137">Figyelmen kívül hagyja az első N objektumokat, és a fennmaradó objektumokat kapja.</span><span class="sxs-lookup"><span data-stu-id="183de-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="183de-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="183de-138">-StartsWith</span></span>
<span data-ttu-id="183de-139">A megadott karakterlánccal kezdődő felhasználók megkeresésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="183de-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="183de-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="183de-140">-UserPrincipalName</span></span>
<span data-ttu-id="183de-141">A felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="183de-141">UPN of the user.</span></span>

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

### <span data-ttu-id="183de-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="183de-142">CommonParameters</span></span>
<span data-ttu-id="183de-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="183de-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="183de-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="183de-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="183de-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="183de-145">INPUTS</span></span>

### <span data-ttu-id="183de-146">System. String</span><span class="sxs-lookup"><span data-stu-id="183de-146">System.String</span></span>

### <span data-ttu-id="183de-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="183de-147">System.Guid</span></span>

## <span data-ttu-id="183de-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="183de-148">OUTPUTS</span></span>

### <span data-ttu-id="183de-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="183de-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="183de-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="183de-150">NOTES</span></span>

## <span data-ttu-id="183de-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="183de-151">RELATED LINKS</span></span>

[<span data-ttu-id="183de-152">Új – AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="183de-152">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)



[<span data-ttu-id="183de-153">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="183de-153">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

