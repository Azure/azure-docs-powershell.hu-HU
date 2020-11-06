---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 983d5049d0ac58671b3d0766b6b4bcf3f05d4d76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495719"
---
# <span data-ttu-id="07936-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="07936-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="07936-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07936-102">SYNOPSIS</span></span>
<span data-ttu-id="07936-103">Szűri az Active Directory-szolgáltatási résztvevőket.</span><span class="sxs-lookup"><span data-stu-id="07936-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07936-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07936-104">SYNTAX</span></span>

### <span data-ttu-id="07936-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="07936-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="07936-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="07936-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="07936-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="07936-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="07936-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07936-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="07936-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07936-109">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="07936-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07936-110">ApplicationObjectParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="07936-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="07936-111">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="07936-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="07936-112">DESCRIPTION</span></span>
<span data-ttu-id="07936-113">Szűri az Active Directory-szolgáltatási résztvevőket.</span><span class="sxs-lookup"><span data-stu-id="07936-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="07936-114">Példák</span><span class="sxs-lookup"><span data-stu-id="07936-114">EXAMPLES</span></span>

### <span data-ttu-id="07936-115">Példa 1 – az AD Service-résztvevők listája</span><span class="sxs-lookup"><span data-stu-id="07936-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="07936-116">Felsorolja a bérlői webhelyhez tartozó összes HIRDETÉSCSOPORT-résztvevőt.</span><span class="sxs-lookup"><span data-stu-id="07936-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="07936-117">Példa 2 – AD-résztvevők listázása a lapozással</span><span class="sxs-lookup"><span data-stu-id="07936-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -First 100
```

<span data-ttu-id="07936-118">Felsorolja az első 100-ös AD-résztvevőket a bérlői webhelyeken.</span><span class="sxs-lookup"><span data-stu-id="07936-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="07936-119">Példa: 3 – a listák egyszerű kézbesítése</span><span class="sxs-lookup"><span data-stu-id="07936-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="07936-120">A "36f81fc3-b00f-48cd-8218-3879f51ff39f" SPN-es szolgáltatásnév listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="07936-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="07936-121">Példa 4 – egy keresési karakterlánccal listázhatja a szolgáltatási résztvevőket</span><span class="sxs-lookup"><span data-stu-id="07936-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="07936-122">Felsorolja az összes olyan AD-szolgáltatót, amelynek a megjelenítendő neve "web"-val kezdődik.</span><span class="sxs-lookup"><span data-stu-id="07936-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="07936-123">Példa: 5 – a listákban szereplő szolgáltatási megbízók</span><span class="sxs-lookup"><span data-stu-id="07936-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzureRmADServicePrincipal
```

<span data-ttu-id="07936-124">Megkapja az "39e64ec6-569b-4030-8e1c-c3c519a05d69" azonosítójú AD-alkalmazást, és a Get-AzureRmADServicePrincipal parancsmaghoz illeszti az adott alkalmazáshoz tartozó összes szolgáltatásnevet.</span><span class="sxs-lookup"><span data-stu-id="07936-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzureRmADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="07936-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07936-125">PARAMETERS</span></span>

### <span data-ttu-id="07936-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="07936-126">-ApplicationId</span></span>
<span data-ttu-id="07936-127">A Service Principal Application azonosító.</span><span class="sxs-lookup"><span data-stu-id="07936-127">The service principal application id.</span></span>

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

### <span data-ttu-id="07936-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="07936-128">-ApplicationObject</span></span>
<span data-ttu-id="07936-129">Annak az alkalmazásobjektum-objektumnak a lekérése, amelynek a szolgáltatását beolvasták.</span><span class="sxs-lookup"><span data-stu-id="07936-129">The application object whose service principal is being retrieved.</span></span>

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

### <span data-ttu-id="07936-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07936-130">-DefaultProfile</span></span>
<span data-ttu-id="07936-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="07936-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07936-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="07936-132">-DisplayName</span></span>
<span data-ttu-id="07936-133">A szolgáltatás fő megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="07936-133">The service principal display name.</span></span>

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

### <span data-ttu-id="07936-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="07936-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="07936-135">A szolgáltatás egyszerű keresési karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="07936-135">The service principal search string.</span></span>

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

### <span data-ttu-id="07936-136">– Első</span><span class="sxs-lookup"><span data-stu-id="07936-136">-First</span></span>
<span data-ttu-id="07936-137">A visszaadni kívánt objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="07936-137">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="07936-138">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="07936-138">-IncludeTotalCount</span></span>
<span data-ttu-id="07936-139">Az adathalmaz objektumainak számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="07936-139">Reports the number of objects in the data set.</span></span> <span data-ttu-id="07936-140">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="07936-140">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="07936-141">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="07936-141">-ObjectId</span></span>
<span data-ttu-id="07936-142">A szolgáltatás megbízójának objektumazonosító-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="07936-142">Object id of the service principal.</span></span>

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

### <span data-ttu-id="07936-143">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="07936-143">-ServicePrincipalName</span></span>
<span data-ttu-id="07936-144">A szolgáltatás SPN-je.</span><span class="sxs-lookup"><span data-stu-id="07936-144">SPN of the service.</span></span>

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

### <span data-ttu-id="07936-145">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="07936-145">-Skip</span></span>
<span data-ttu-id="07936-146">Figyelmen kívül hagyja az első N objektumokat, és a fennmaradó objektumokat kapja.</span><span class="sxs-lookup"><span data-stu-id="07936-146">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="07936-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07936-147">CommonParameters</span></span>
<span data-ttu-id="07936-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="07936-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07936-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07936-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07936-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07936-150">INPUTS</span></span>

### <span data-ttu-id="07936-151">System. String</span><span class="sxs-lookup"><span data-stu-id="07936-151">System.String</span></span>

### <span data-ttu-id="07936-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="07936-152">System.Guid</span></span>

### <span data-ttu-id="07936-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="07936-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="07936-154">Paraméterek: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="07936-154">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="07936-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07936-155">OUTPUTS</span></span>

### <span data-ttu-id="07936-156">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="07936-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="07936-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07936-157">NOTES</span></span>

## <span data-ttu-id="07936-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07936-158">RELATED LINKS</span></span>

[<span data-ttu-id="07936-159">Új – AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="07936-159">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="07936-160">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="07936-160">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="07936-161">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="07936-161">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="07936-162">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="07936-162">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="07936-163">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="07936-163">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

