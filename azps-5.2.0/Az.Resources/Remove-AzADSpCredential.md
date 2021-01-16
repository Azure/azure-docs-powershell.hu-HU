---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: bcb33f87b85eb6ad5bce9ba812ebccb4d154e920
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363004"
---
# <span data-ttu-id="e4bff-101">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e4bff-101">Remove-AzADSpCredential</span></span>

## <span data-ttu-id="e4bff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4bff-102">SYNOPSIS</span></span>
<span data-ttu-id="e4bff-103">Eltávolítja a hitelesítő adatokat egy egyszerű szolgáltatásnévből.</span><span class="sxs-lookup"><span data-stu-id="e4bff-103">Removes a credential from a service principal.</span></span>

## <span data-ttu-id="e4bff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e4bff-104">SYNTAX</span></span>

### <span data-ttu-id="e4bff-105">ObjectIdWithKeyIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e4bff-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADSpCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4bff-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4bff-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4bff-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4bff-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4bff-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4bff-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4bff-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e4bff-109">DESCRIPTION</span></span>
<span data-ttu-id="e4bff-110">A Remove-AzADSpCredential parancsmagot használva eltávolíthatja a hitelesítő adatokat a egyszerű szolgáltatásnévből, ha feltörik, vagy a hitelesítőkulcs-visszaállítás elévülésének részeként.</span><span class="sxs-lookup"><span data-stu-id="e4bff-110">The Remove-AzADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="e4bff-111">A rendszer a egyszerű szolgáltatásnevet az objektumazonosító vagy az egyszerű szolgáltatásnév (SPN) megszolgáltatása alapján azonosítja.</span><span class="sxs-lookup"><span data-stu-id="e4bff-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="e4bff-112">Az eltávolítható hitelesítő adatokat a kulcsazonosító azonosítja, ha törölni szeretne egy egyéni hitelesítő adatokat, vagy ha a "Mind" kapcsolóval törli a szolgáltatásnévvel társított összes hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="e4bff-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="e4bff-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e4bff-113">EXAMPLES</span></span>

### <span data-ttu-id="e4bff-114">1. példa: Adott hitelesítő adat eltávolítása egyszerű szolgáltatásnévből</span><span class="sxs-lookup"><span data-stu-id="e4bff-114">Example 1: Remove a specific credential from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="e4bff-115">A (7663d3fb-6f86-4352-9ab1-09534157ebb) kulcsazonosítóval eltávolítja a (7663d3fb-6f86-4352-9e6d-cf9d50d5ee82) azonosítójú egyszerű szolgáltatásnévből.</span><span class="sxs-lookup"><span data-stu-id="e4bff-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="e4bff-116">2. példa: Az összes hitelesítő adat eltávolítása egyszerű szolgáltatásnévből</span><span class="sxs-lookup"><span data-stu-id="e4bff-116">Example 2: Remove all credentials from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="e4bff-117">Eltávolítja az összes hitelesítő adatokat a egyszerű szolgáltatásnévből, az SPN " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="e4bff-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="e4bff-118">3. példa: Az egyszerű szolgáltatásnév összes hitelesítő adatának eltávolítása pipázással</span><span class="sxs-lookup"><span data-stu-id="e4bff-118">Example 3: Remove all credentials from a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

<span data-ttu-id="e4bff-119">A (7663d3fb-6f86-4352-9e6d-cf9d50d5ee82) objektumazonosítóval és a Remove-AzADSpCredential-parancsmaghoz vezető összes hitelesítő adatnak a szolgáltatásnévből való eltávolításához szükséges egyszerű szolgáltatásnévvel.</span><span class="sxs-lookup"><span data-stu-id="e4bff-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="e4bff-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4bff-120">PARAMETERS</span></span>

### <span data-ttu-id="e4bff-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4bff-121">-DefaultProfile</span></span>
<span data-ttu-id="e4bff-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e4bff-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4bff-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e4bff-123">-DisplayName</span></span>
<span data-ttu-id="e4bff-124">A szolgáltatásnév megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="e4bff-124">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4bff-125">-Force</span><span class="sxs-lookup"><span data-stu-id="e4bff-125">-Force</span></span>
<span data-ttu-id="e4bff-126">Váltás a hitelesítő adatok törléséhez megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="e4bff-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="e4bff-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="e4bff-127">-KeyId</span></span>
<span data-ttu-id="e4bff-128">Az eltávolítható hitelesítőadat-kulcs.</span><span class="sxs-lookup"><span data-stu-id="e4bff-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="e4bff-129">A egyszerű szolgáltatásnév kulcsazonosítóit a Get-AzADSpCredential használatával lehet beszerezni.</span><span class="sxs-lookup"><span data-stu-id="e4bff-129">The key Ids for a service principal can be obtained using the Get-AzADSpCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet, ServicePrincipalObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4bff-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e4bff-130">-ObjectId</span></span>
<span data-ttu-id="e4bff-131">A szolgáltatásnév objektumazonosítója, amelyből el szeretné távolítani a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="e4bff-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4bff-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4bff-132">-PassThru</span></span>
<span data-ttu-id="e4bff-133">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="e4bff-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="e4bff-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e4bff-134">-ServicePrincipalName</span></span>
<span data-ttu-id="e4bff-135">A hitelesítő adatok eltávolításához használt egyszerű szolgáltatásnév (SPN) neve.</span><span class="sxs-lookup"><span data-stu-id="e4bff-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4bff-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="e4bff-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="e4bff-137">Az egyszerű szolgáltatásobjektum, amelyből el szeretné távolítani a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="e4bff-137">The service principal object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4bff-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4bff-138">-Confirm</span></span>
<span data-ttu-id="e4bff-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e4bff-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4bff-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4bff-140">-WhatIf</span></span>
<span data-ttu-id="e4bff-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e4bff-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4bff-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4bff-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4bff-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4bff-143">CommonParameters</span></span>
<span data-ttu-id="e4bff-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4bff-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4bff-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4bff-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4bff-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4bff-146">INPUTS</span></span>

### <span data-ttu-id="e4bff-147">System.String</span><span class="sxs-lookup"><span data-stu-id="e4bff-147">System.String</span></span>

### <span data-ttu-id="e4bff-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e4bff-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="e4bff-149">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e4bff-149">System.Guid</span></span>

## <span data-ttu-id="e4bff-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4bff-150">OUTPUTS</span></span>

### <span data-ttu-id="e4bff-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e4bff-151">System.Boolean</span></span>

## <span data-ttu-id="e4bff-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e4bff-152">NOTES</span></span>

## <span data-ttu-id="e4bff-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4bff-153">RELATED LINKS</span></span>

[<span data-ttu-id="e4bff-154">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e4bff-154">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="e4bff-155">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e4bff-155">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="e4bff-156">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e4bff-156">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

