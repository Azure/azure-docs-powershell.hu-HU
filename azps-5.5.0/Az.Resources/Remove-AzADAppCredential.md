---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: f6344590828663a0cf44d96d6fe733adff8757c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158458"
---
# <span data-ttu-id="b9be7-101">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b9be7-101">Remove-AzADAppCredential</span></span>

## <span data-ttu-id="b9be7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9be7-102">SYNOPSIS</span></span>
<span data-ttu-id="b9be7-103">Eltávolít egy hitelesítő adatokat egy alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="b9be7-103">Removes a credential from an application.</span></span>

## <span data-ttu-id="b9be7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b9be7-104">SYNTAX</span></span>

### <span data-ttu-id="b9be7-105">ApplicationObjectIdWithKeyIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9be7-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADAppCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9be7-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9be7-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9be7-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9be7-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9be7-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9be7-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9be7-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b9be7-109">DESCRIPTION</span></span>
<span data-ttu-id="b9be7-110">A Remove-AzADAppCredential parancsmagot használva eltávolíthatja a hitelesítő adatokat az alkalmazásokból biztonsági hiba vagy a hitelesítő adatok kulcsának elévülése részeként.</span><span class="sxs-lookup"><span data-stu-id="b9be7-110">The Remove-AzADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="b9be7-111">Az alkalmazás az objektumazonosító vagy az AppId megszolgáltatásával azonosítható.</span><span class="sxs-lookup"><span data-stu-id="b9be7-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="b9be7-112">Az eltávolítható hitelesítő adatokat a kulcsazonosító azonosítja.</span><span class="sxs-lookup"><span data-stu-id="b9be7-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="b9be7-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b9be7-113">EXAMPLES</span></span>

### <span data-ttu-id="b9be7-114">1. példa: Adott hitelesítő adatok eltávolítása egy alkalmazásból</span><span class="sxs-lookup"><span data-stu-id="b9be7-114">Example 1: Remove a specific credential from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="b9be7-115">Eltávolítja a (9044423a-60a3-45ac-9ab1-09534157ebb) azonosítójú hitelesítő adatokat az alkalmazásból a (7663d3fb-6f86-4352-9e6d-cf9d50d5ee82) objektumazonosítóval.</span><span class="sxs-lookup"><span data-stu-id="b9be7-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="b9be7-116">2. példa: Az összes hitelesítő adat eltávolítása egy alkalmazásból</span><span class="sxs-lookup"><span data-stu-id="b9be7-116">Example 2: Remove all credentials from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="b9be7-117">A (4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58) azonosítójú alkalmazás összes hitelesítő adatának eltávolítása az alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="b9be7-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="b9be7-118">3. példa: Az összes hitelesítő adat eltávolítása pipázás használatával</span><span class="sxs-lookup"><span data-stu-id="b9be7-118">Example 3: Remove all credentials using piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

<span data-ttu-id="b9be7-119">A (7663d3fb-6f86-4352-9e6d-cf9d50d5ee82) objektumazonosítóval és az Remove-AzADAppCredential-parancsmaghoz használtcsövekkel együtt beveszi az alkalmazást, és eltávolítja az alkalmazás összes hitelesítő adatát.</span><span class="sxs-lookup"><span data-stu-id="b9be7-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="b9be7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9be7-120">PARAMETERS</span></span>

### <span data-ttu-id="b9be7-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b9be7-121">-ApplicationId</span></span>
<span data-ttu-id="b9be7-122">Annak az alkalmazásnak az azonosítója, amelyből el szeretné távolítani a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="b9be7-122">The id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9be7-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="b9be7-123">-ApplicationObject</span></span>
<span data-ttu-id="b9be7-124">Az az alkalmazásobjektum, amelyből el szeretné távolítani a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="b9be7-124">The application object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9be7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9be7-125">-DefaultProfile</span></span>
<span data-ttu-id="b9be7-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b9be7-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9be7-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b9be7-127">-DisplayName</span></span>
<span data-ttu-id="b9be7-128">Az alkalmazás megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="b9be7-128">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9be7-129">-Force</span><span class="sxs-lookup"><span data-stu-id="b9be7-129">-Force</span></span>
<span data-ttu-id="b9be7-130">Váltás a hitelesítő adatok törléséhez megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="b9be7-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="b9be7-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="b9be7-131">-KeyId</span></span>
<span data-ttu-id="b9be7-132">Az eltávolítható hitelesítőadat-kulcs.</span><span class="sxs-lookup"><span data-stu-id="b9be7-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="b9be7-133">Az alkalmazás kulcsazonosítói a Get-AzADAppCredential segítségével szerezhetők be.</span><span class="sxs-lookup"><span data-stu-id="b9be7-133">The key Ids for the application can be obtained using the Get-AzADAppCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9be7-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b9be7-134">-ObjectId</span></span>
<span data-ttu-id="b9be7-135">Annak az alkalmazásnak az objektumazonosítója, amelyből el szeretné távolítani a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="b9be7-135">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9be7-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9be7-136">-PassThru</span></span>
<span data-ttu-id="b9be7-137">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="b9be7-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="b9be7-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9be7-138">-Confirm</span></span>
<span data-ttu-id="b9be7-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b9be7-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9be7-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9be7-140">-WhatIf</span></span>
<span data-ttu-id="b9be7-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b9be7-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9be7-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9be7-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9be7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9be7-143">CommonParameters</span></span>
<span data-ttu-id="b9be7-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9be7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9be7-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9be7-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9be7-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9be7-146">INPUTS</span></span>

### <span data-ttu-id="b9be7-147">System.String</span><span class="sxs-lookup"><span data-stu-id="b9be7-147">System.String</span></span>

### <span data-ttu-id="b9be7-148">System.Guid</span><span class="sxs-lookup"><span data-stu-id="b9be7-148">System.Guid</span></span>

### <span data-ttu-id="b9be7-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="b9be7-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="b9be7-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9be7-150">OUTPUTS</span></span>

### <span data-ttu-id="b9be7-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b9be7-151">System.Boolean</span></span>

## <span data-ttu-id="b9be7-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b9be7-152">NOTES</span></span>

## <span data-ttu-id="b9be7-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9be7-153">RELATED LINKS</span></span>

[<span data-ttu-id="b9be7-154">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b9be7-154">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="b9be7-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b9be7-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="b9be7-156">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b9be7-156">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
