---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: 10d95102058c759f9b2641f233bd590364945c71
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849046"
---
# <span data-ttu-id="27784-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="27784-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="27784-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27784-102">SYNOPSIS</span></span>
<span data-ttu-id="27784-103">Szűri az Active Directory-szolgáltatási résztvevőket.</span><span class="sxs-lookup"><span data-stu-id="27784-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27784-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27784-104">SYNTAX</span></span>

### <span data-ttu-id="27784-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="27784-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="27784-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="27784-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="27784-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="27784-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="27784-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27784-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="27784-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27784-109">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="27784-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27784-110">ApplicationObjectParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="27784-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="27784-111">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="27784-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="27784-112">DESCRIPTION</span></span>
<span data-ttu-id="27784-113">Szűri az Active Directory-szolgáltatási résztvevőket.</span><span class="sxs-lookup"><span data-stu-id="27784-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="27784-114">Példák</span><span class="sxs-lookup"><span data-stu-id="27784-114">EXAMPLES</span></span>

### <span data-ttu-id="27784-115">Példa 1 – az AD Service-résztvevők listája</span><span class="sxs-lookup"><span data-stu-id="27784-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="27784-116">Felsorolja a bérlői webhelyhez tartozó összes HIRDETÉSCSOPORT-résztvevőt.</span><span class="sxs-lookup"><span data-stu-id="27784-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="27784-117">Példa 2 – AD-résztvevők listázása a lapozással</span><span class="sxs-lookup"><span data-stu-id="27784-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -First 100
```

<span data-ttu-id="27784-118">Felsorolja az első 100-ös AD-résztvevőket a bérlői webhelyeken.</span><span class="sxs-lookup"><span data-stu-id="27784-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="27784-119">Példa: 3 – a listák egyszerű kézbesítése</span><span class="sxs-lookup"><span data-stu-id="27784-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="27784-120">A "36f81fc3-b00f-48cd-8218-3879f51ff39f" SPN-es szolgáltatásnév listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="27784-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="27784-121">Példa 4 – egy keresési karakterlánccal listázhatja a szolgáltatási résztvevőket</span><span class="sxs-lookup"><span data-stu-id="27784-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="27784-122">Felsorolja az összes olyan AD-szolgáltatót, amelynek a megjelenítendő neve "web"-val kezdődik.</span><span class="sxs-lookup"><span data-stu-id="27784-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="27784-123">Példa: 5 – a listákban szereplő szolgáltatási megbízók</span><span class="sxs-lookup"><span data-stu-id="27784-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzureRmADServicePrincipal
```

<span data-ttu-id="27784-124">Megkapja az "39e64ec6-569b-4030-8e1c-c3c519a05d69" azonosítójú AD-alkalmazást, és a Get-AzureRmADServicePrincipal parancsmaghoz illeszti az adott alkalmazáshoz tartozó összes szolgáltatásnevet.</span><span class="sxs-lookup"><span data-stu-id="27784-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzureRmADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="27784-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27784-125">PARAMETERS</span></span>

### <span data-ttu-id="27784-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="27784-126">-ApplicationId</span></span>
<span data-ttu-id="27784-127">A Service Principal Application azonosító.</span><span class="sxs-lookup"><span data-stu-id="27784-127">The service principal application id.</span></span>

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

### <span data-ttu-id="27784-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="27784-128">-ApplicationObject</span></span>
<span data-ttu-id="27784-129">Annak az alkalmazásobjektum-objektumnak a lekérése, amelynek a szolgáltatását beolvasták.</span><span class="sxs-lookup"><span data-stu-id="27784-129">The application object whose service principal is being retrieved.</span></span>

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

### <span data-ttu-id="27784-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27784-130">-DefaultProfile</span></span>
<span data-ttu-id="27784-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="27784-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27784-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="27784-132">-DisplayName</span></span>
<span data-ttu-id="27784-133">A szolgáltatás fő megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="27784-133">The service principal display name.</span></span>

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

### <span data-ttu-id="27784-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="27784-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="27784-135">A szolgáltatás egyszerű keresési karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="27784-135">The service principal search string.</span></span>

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

### <span data-ttu-id="27784-136">– Első</span><span class="sxs-lookup"><span data-stu-id="27784-136">-First</span></span>
<span data-ttu-id="27784-137">A visszaadni kívánt objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="27784-137">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="27784-138">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="27784-138">-IncludeTotalCount</span></span>
<span data-ttu-id="27784-139">Az adathalmaz objektumainak számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="27784-139">Reports the number of objects in the data set.</span></span> <span data-ttu-id="27784-140">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="27784-140">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="27784-141">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="27784-141">-ObjectId</span></span>
<span data-ttu-id="27784-142">A szolgáltatás megbízójának objektumazonosító-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="27784-142">Object id of the service principal.</span></span>

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

### <span data-ttu-id="27784-143">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="27784-143">-ServicePrincipalName</span></span>
<span data-ttu-id="27784-144">A szolgáltatás SPN-je.</span><span class="sxs-lookup"><span data-stu-id="27784-144">SPN of the service.</span></span>

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

### <span data-ttu-id="27784-145">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="27784-145">-Skip</span></span>
<span data-ttu-id="27784-146">Figyelmen kívül hagyja az első N objektumokat, és a fennmaradó objektumokat kapja.</span><span class="sxs-lookup"><span data-stu-id="27784-146">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="27784-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27784-147">CommonParameters</span></span>
<span data-ttu-id="27784-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27784-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27784-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27784-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27784-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27784-150">INPUTS</span></span>

### <span data-ttu-id="27784-151">System. String</span><span class="sxs-lookup"><span data-stu-id="27784-151">System.String</span></span>

### <span data-ttu-id="27784-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="27784-152">System.Guid</span></span>

### <span data-ttu-id="27784-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="27784-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="27784-154">Paraméterek: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="27784-154">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="27784-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27784-155">OUTPUTS</span></span>

### <span data-ttu-id="27784-156">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="27784-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="27784-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27784-157">NOTES</span></span>

## <span data-ttu-id="27784-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27784-158">RELATED LINKS</span></span>

[<span data-ttu-id="27784-159">Új – AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="27784-159">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)



[<span data-ttu-id="27784-160">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="27784-160">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="27784-161">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="27784-161">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="27784-162">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="27784-162">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

