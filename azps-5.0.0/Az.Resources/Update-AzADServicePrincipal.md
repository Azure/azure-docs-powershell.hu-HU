---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: 05bd5f7997c83c2be6b50faf0e6d88ee7413a773
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302447"
---
# <span data-ttu-id="c84f5-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c84f5-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="c84f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c84f5-102">SYNOPSIS</span></span>
<span data-ttu-id="c84f5-103">Frissít egy meglévő Azure Active Directory-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="c84f5-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="c84f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c84f5-104">SYNTAX</span></span>

### <span data-ttu-id="c84f5-105">SpObjectIdWithDisplayNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c84f5-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c84f5-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c84f5-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c84f5-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c84f5-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c84f5-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c84f5-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c84f5-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="c84f5-109">DESCRIPTION</span></span>
<span data-ttu-id="c84f5-110">Frissít egy meglévő Azure Active Directory-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="c84f5-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="c84f5-111">Ha frissíteni szeretné az ehhez a szolgáltatáshoz tartozó hitelesítő adatokat, használja az New-AzADSpCredential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c84f5-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="c84f5-112">Ha frissíteni szeretné a mögöttes alkalmazáshoz tartozó tulajdonságokat, használja az Update-AzADApplication parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c84f5-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="c84f5-113">Példák</span><span class="sxs-lookup"><span data-stu-id="c84f5-113">EXAMPLES</span></span>

### <span data-ttu-id="c84f5-114">Példa 1: egy egyszerű szolgáltatásnév megjelenítendő nevének frissítése</span><span class="sxs-lookup"><span data-stu-id="c84f5-114">Example 1: Update the display name of a service principal</span></span>

```powershell
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="c84f5-115">Frissíti a "784136ca-3ae2-4fdd-a388-89d793e7c780" azonosítójú, "MyNewDisplayName" azonosítójú szolgáltatásnév megjelenítendő nevét.</span><span class="sxs-lookup"><span data-stu-id="c84f5-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="c84f5-116">2. példa: a megbízó megjelenítendő nevének frissítése csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="c84f5-116">Example 2: Update the display name of a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="c84f5-117">Megkapja a "784136ca-3ae2-4fdd-a388-89d793e7c780" azonosítójú szolgáltatásnevet, valamint az Update-AzADServicePrincipal parancsmagot tartalmazó csöveket, így a szolgáltatás nevének neve a "MyNewDisplayName" névre frissíthető.</span><span class="sxs-lookup"><span data-stu-id="c84f5-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

### <span data-ttu-id="c84f5-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="c84f5-118">Example 3</span></span>

<span data-ttu-id="c84f5-119">Frissít egy meglévő Azure Active Directory-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="c84f5-119">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="c84f5-120">autogenerated</span><span class="sxs-lookup"><span data-stu-id="c84f5-120">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzADServicePrincipal -IdentifierUri https://mySecretApp1 -ObjectId 00000000-0000-0000-0000-00000000000000000
```

## <span data-ttu-id="c84f5-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c84f5-121">PARAMETERS</span></span>

### <span data-ttu-id="c84f5-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c84f5-122">-ApplicationId</span></span>
<span data-ttu-id="c84f5-123">A frissítendő szolgáltatásnevet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c84f5-123">The application id of the service principal to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpApplicationIdWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c84f5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c84f5-124">-DefaultProfile</span></span>
<span data-ttu-id="c84f5-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c84f5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c84f5-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c84f5-126">-DisplayName</span></span>
<span data-ttu-id="c84f5-127">A szolgáltatás megbízójának megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="c84f5-127">The display name for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet, SPNWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c84f5-128">-Kezdőlap</span><span class="sxs-lookup"><span data-stu-id="c84f5-128">-Homepage</span></span>
<span data-ttu-id="c84f5-129">A szolgáltatás fő weboldala.</span><span class="sxs-lookup"><span data-stu-id="c84f5-129">The homepage for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c84f5-130">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="c84f5-130">-IdentifierUri</span></span>
<span data-ttu-id="c84f5-131">A szolgáltatásnevet azonosító URI (ok).</span><span class="sxs-lookup"><span data-stu-id="c84f5-131">The identifier URI(s) for the service principal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c84f5-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c84f5-132">-InputObject</span></span>
<span data-ttu-id="c84f5-133">A frissítendő szolgáltatásnevet képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="c84f5-133">The object representing the service principal to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c84f5-134">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="c84f5-134">-KeyCredential</span></span>
<span data-ttu-id="c84f5-135">A fő hitelesítő adatok a szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="c84f5-135">The key credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.KeyCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c84f5-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c84f5-136">-ObjectId</span></span>
<span data-ttu-id="c84f5-137">A frissítendő szolgáltatásnevet azonosító.</span><span class="sxs-lookup"><span data-stu-id="c84f5-137">The object id of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c84f5-138">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="c84f5-138">-PasswordCredential</span></span>
<span data-ttu-id="c84f5-139">A szolgáltatóhoz tartozó jelszó (ok) a hitelesítő adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="c84f5-139">The password credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.PasswordCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c84f5-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c84f5-140">-ServicePrincipalName</span></span>
<span data-ttu-id="c84f5-141">A frissítendő szolgáltatásnév.</span><span class="sxs-lookup"><span data-stu-id="c84f5-141">The SPN of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c84f5-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c84f5-142">-Confirm</span></span>
<span data-ttu-id="c84f5-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c84f5-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c84f5-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c84f5-144">-WhatIf</span></span>
<span data-ttu-id="c84f5-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c84f5-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c84f5-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c84f5-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c84f5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c84f5-147">CommonParameters</span></span>
<span data-ttu-id="c84f5-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c84f5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c84f5-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c84f5-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c84f5-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c84f5-150">INPUTS</span></span>

### <span data-ttu-id="c84f5-151">System. String</span><span class="sxs-lookup"><span data-stu-id="c84f5-151">System.String</span></span>

### <span data-ttu-id="c84f5-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c84f5-152">System.Guid</span></span>

### <span data-ttu-id="c84f5-153">Microsoft. Azure. Command. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c84f5-153">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="c84f5-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c84f5-154">OUTPUTS</span></span>

### <span data-ttu-id="c84f5-155">Microsoft. Azure. Command. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c84f5-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="c84f5-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c84f5-156">NOTES</span></span>

## <span data-ttu-id="c84f5-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c84f5-157">RELATED LINKS</span></span>