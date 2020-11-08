---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: b467d629b578e9f9883dac4c0a8e268f9007a373
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188209"
---
# <span data-ttu-id="6f43b-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6f43b-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="6f43b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f43b-102">SYNOPSIS</span></span>
<span data-ttu-id="6f43b-103">Szűri az Active Directory-szolgáltatási résztvevőket.</span><span class="sxs-lookup"><span data-stu-id="6f43b-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="6f43b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f43b-104">SYNTAX</span></span>

### <span data-ttu-id="6f43b-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6f43b-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6f43b-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f43b-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6f43b-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f43b-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6f43b-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f43b-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6f43b-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f43b-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6f43b-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f43b-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6f43b-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f43b-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="6f43b-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f43b-112">DESCRIPTION</span></span>
<span data-ttu-id="6f43b-113">Szűri az Active Directory-szolgáltatási résztvevőket.</span><span class="sxs-lookup"><span data-stu-id="6f43b-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="6f43b-114">Példák</span><span class="sxs-lookup"><span data-stu-id="6f43b-114">EXAMPLES</span></span>

### <span data-ttu-id="6f43b-115">1. példa: AD-szolgáltatói résztvevők listázása</span><span class="sxs-lookup"><span data-stu-id="6f43b-115">Example 1: List AD service principals</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="6f43b-116">Felsorolja a bérlői webhelyhez tartozó összes HIRDETÉSCSOPORT-résztvevőt.</span><span class="sxs-lookup"><span data-stu-id="6f43b-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="6f43b-117">2. példa: az AD-résztvevők listázása a lapozással</span><span class="sxs-lookup"><span data-stu-id="6f43b-117">Example 2: List AD service principals using paging</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="6f43b-118">Felsorolja az első 100-ös AD-résztvevőket a bérlői webhelyeken.</span><span class="sxs-lookup"><span data-stu-id="6f43b-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="6f43b-119">3. példa: a lista-szolgáltatási résztvevőket SPN-ként</span><span class="sxs-lookup"><span data-stu-id="6f43b-119">Example 3: List service principals by SPN</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="6f43b-120">A "36f81fc3-b00f-48cd-8218-3879f51ff39f" SPN-es szolgáltatásnév listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="6f43b-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="6f43b-121">4. példa: a lista-szolgáltatási résztvevők keresése karakterlánc szerint</span><span class="sxs-lookup"><span data-stu-id="6f43b-121">Example 4: List service principals by search string</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="6f43b-122">Felsorolja az összes olyan AD-szolgáltatót, amelynek a megjelenítendő neve "web"-val kezdődik.</span><span class="sxs-lookup"><span data-stu-id="6f43b-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="6f43b-123">5. példa: a lista-szolgáltatási megbízók</span><span class="sxs-lookup"><span data-stu-id="6f43b-123">Example 5: List service principals by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="6f43b-124">Megkapja az "39e64ec6-569b-4030-8e1c-c3c519a05d69" azonosítójú AD-alkalmazást, és a Get-AzADServicePrincipal parancsmaghoz illeszti az adott alkalmazáshoz tartozó összes szolgáltatásnevet.</span><span class="sxs-lookup"><span data-stu-id="6f43b-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="6f43b-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f43b-125">PARAMETERS</span></span>

### <span data-ttu-id="6f43b-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="6f43b-126">-ApplicationId</span></span>
<span data-ttu-id="6f43b-127">A Service Principal Application azonosító.</span><span class="sxs-lookup"><span data-stu-id="6f43b-127">The service principal application id.</span></span>

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

### <span data-ttu-id="6f43b-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="6f43b-128">-ApplicationObject</span></span>
<span data-ttu-id="6f43b-129">Annak az alkalmazásobjektum-objektumnak a lekérése, amelynek a szolgáltatását beolvasták.</span><span class="sxs-lookup"><span data-stu-id="6f43b-129">The application object whose service principal is being retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f43b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f43b-130">-DefaultProfile</span></span>
<span data-ttu-id="6f43b-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6f43b-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f43b-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6f43b-132">-DisplayName</span></span>
<span data-ttu-id="6f43b-133">A szolgáltatás fő megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="6f43b-133">The service principal display name.</span></span>

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

### <span data-ttu-id="6f43b-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="6f43b-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="6f43b-135">A szolgáltatás egyszerű keresési karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="6f43b-135">The service principal search string.</span></span>

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

### <span data-ttu-id="6f43b-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6f43b-136">-ObjectId</span></span>
<span data-ttu-id="6f43b-137">A szolgáltatás megbízójának objektumazonosító-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6f43b-137">Object id of the service principal.</span></span>

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

### <span data-ttu-id="6f43b-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="6f43b-138">-ServicePrincipalName</span></span>
<span data-ttu-id="6f43b-139">A szolgáltatás SPN-je.</span><span class="sxs-lookup"><span data-stu-id="6f43b-139">SPN of the service.</span></span>

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

### <span data-ttu-id="6f43b-140">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="6f43b-140">-IncludeTotalCount</span></span>
<span data-ttu-id="6f43b-141">Az adathalmaz objektumainak számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="6f43b-141">Reports the number of objects in the data set.</span></span> <span data-ttu-id="6f43b-142">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="6f43b-142">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="6f43b-143">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="6f43b-143">-Skip</span></span>
<span data-ttu-id="6f43b-144">Figyelmen kívül hagyja az első N objektumokat, és a fennmaradó objektumokat kapja.</span><span class="sxs-lookup"><span data-stu-id="6f43b-144">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="6f43b-145">– Első</span><span class="sxs-lookup"><span data-stu-id="6f43b-145">-First</span></span>
<span data-ttu-id="6f43b-146">A visszaadni kívánt objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="6f43b-146">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="6f43b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f43b-147">CommonParameters</span></span>
<span data-ttu-id="6f43b-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f43b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f43b-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6f43b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f43b-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f43b-150">INPUTS</span></span>

### <span data-ttu-id="6f43b-151">System. String</span><span class="sxs-lookup"><span data-stu-id="6f43b-151">System.String</span></span>

### <span data-ttu-id="6f43b-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="6f43b-152">System.Guid</span></span>

### <span data-ttu-id="6f43b-153">Microsoft. Azure. Command. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="6f43b-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="6f43b-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f43b-154">OUTPUTS</span></span>

### <span data-ttu-id="6f43b-155">Microsoft. Azure. Command. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6f43b-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="6f43b-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f43b-156">NOTES</span></span>

## <span data-ttu-id="6f43b-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f43b-157">RELATED LINKS</span></span>

[<span data-ttu-id="6f43b-158">Új – AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6f43b-158">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="6f43b-159">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6f43b-159">Update-AzADServicePrincipal</span></span>](./Update-AzADServicePrincipal.md)

[<span data-ttu-id="6f43b-160">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6f43b-160">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="6f43b-161">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="6f43b-161">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="6f43b-162">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="6f43b-162">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

