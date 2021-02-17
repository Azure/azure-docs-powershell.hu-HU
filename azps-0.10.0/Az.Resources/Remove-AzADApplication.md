---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: 956fcf09006e8e65d029bb5e380abc5de0e15c17
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399923"
---
# <span data-ttu-id="90230-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="90230-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="90230-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90230-102">SYNOPSIS</span></span>
<span data-ttu-id="90230-103">Törli az Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="90230-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="90230-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="90230-104">SYNTAX</span></span>

### <span data-ttu-id="90230-105">ObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="90230-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90230-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="90230-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90230-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="90230-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90230-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90230-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90230-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="90230-109">DESCRIPTION</span></span>
<span data-ttu-id="90230-110">Törli az Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="90230-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="90230-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="90230-111">EXAMPLES</span></span>

### <span data-ttu-id="90230-112">1. példa: Alkalmazás eltávolítása objektumazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="90230-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="90230-113">Eltávolítja a bérlői webhelyről a "b4cd1619-80b3-4cfb-9f8f-9f233425738" objektumazonosítójú alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="90230-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="90230-114">2. példa: Alkalmazás eltávolítása alkalmazásazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="90230-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="90230-115">Eltávolítja az "f9c5ea4f-28f0-401a-a491-491a037fa346" azonosítójú alkalmazást a bérlőből.</span><span class="sxs-lookup"><span data-stu-id="90230-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="90230-116">3. példa: Alkalmazás eltávolítása pipázással</span><span class="sxs-lookup"><span data-stu-id="90230-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="90230-117">A (b4cd1619-80b3-4cfb-9f8f-9f233425738) objektumazonosítót, valamint a Remove-AzADApplication-parancsmagnak az alkalmazást a bérlői webhelyről való eltávolításához szükségescsövekkel együtt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="90230-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="90230-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90230-118">PARAMETERS</span></span>

### <span data-ttu-id="90230-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="90230-119">-ApplicationId</span></span>
<span data-ttu-id="90230-120">Az eltávolítható alkalmazás alkalmazásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="90230-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="90230-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90230-121">-DefaultProfile</span></span>
<span data-ttu-id="90230-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="90230-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90230-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="90230-123">-DisplayName</span></span>
<span data-ttu-id="90230-124">Az alkalmazás megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="90230-124">The display name of the application.</span></span>

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

### <span data-ttu-id="90230-125">-Force</span><span class="sxs-lookup"><span data-stu-id="90230-125">-Force</span></span>
<span data-ttu-id="90230-126">Váltás alkalmazás törléséhez megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="90230-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="90230-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90230-127">-InputObject</span></span>
<span data-ttu-id="90230-128">Az eltávolítható alkalmazást képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="90230-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90230-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="90230-129">-ObjectId</span></span>
<span data-ttu-id="90230-130">A törölni kívánt alkalmazás objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="90230-130">The object id of the application to delete.</span></span>

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

### <span data-ttu-id="90230-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90230-131">-PassThru</span></span>
<span data-ttu-id="90230-132">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="90230-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="90230-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90230-133">-Confirm</span></span>
<span data-ttu-id="90230-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="90230-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90230-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90230-135">-WhatIf</span></span>
<span data-ttu-id="90230-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="90230-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90230-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="90230-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90230-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90230-138">CommonParameters</span></span>
<span data-ttu-id="90230-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90230-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90230-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90230-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90230-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90230-141">INPUTS</span></span>

### <span data-ttu-id="90230-142">System.Guid</span><span class="sxs-lookup"><span data-stu-id="90230-142">System.Guid</span></span>

### <span data-ttu-id="90230-143">System.String</span><span class="sxs-lookup"><span data-stu-id="90230-143">System.String</span></span>

### <span data-ttu-id="90230-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="90230-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="90230-145">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="90230-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="90230-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90230-146">OUTPUTS</span></span>

### <span data-ttu-id="90230-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="90230-147">System.Boolean</span></span>

## <span data-ttu-id="90230-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="90230-148">NOTES</span></span>
<span data-ttu-id="90230-149">Kulcsszavak: azure, Az, arm, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, telepítés</span><span class="sxs-lookup"><span data-stu-id="90230-149">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="90230-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90230-150">RELATED LINKS</span></span>

[<span data-ttu-id="90230-151">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="90230-151">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="90230-152">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="90230-152">Get-AzADApplication</span></span>](./Get-AzADApplication.md)


[<span data-ttu-id="90230-153">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="90230-153">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

