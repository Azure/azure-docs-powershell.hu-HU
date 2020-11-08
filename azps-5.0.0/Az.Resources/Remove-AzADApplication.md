---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: e27dcc838499e742c887f60a30021d8ac99277f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186554"
---
# <span data-ttu-id="7d9ae-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="7d9ae-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="7d9ae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d9ae-102">SYNOPSIS</span></span>
<span data-ttu-id="7d9ae-103">Törli az Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="7d9ae-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="7d9ae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d9ae-104">SYNTAX</span></span>

### <span data-ttu-id="7d9ae-105">ObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7d9ae-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d9ae-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d9ae-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d9ae-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d9ae-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d9ae-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d9ae-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d9ae-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d9ae-109">DESCRIPTION</span></span>
<span data-ttu-id="7d9ae-110">Törli az Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="7d9ae-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="7d9ae-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7d9ae-111">EXAMPLES</span></span>

### <span data-ttu-id="7d9ae-112">1. példa: az alkalmazás objektum-azonosítójának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7d9ae-112">Example 1: Remove application by object id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="7d9ae-113">Eltávolítja az "b4cd1619-80b3-4cfb-9f8f-9f2333425738" azonosítójú alkalmazást a bérlői webhelyről.</span><span class="sxs-lookup"><span data-stu-id="7d9ae-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="7d9ae-114">2. példa: alkalmazás-azonosító eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7d9ae-114">Example 2: Remove application by application id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="7d9ae-115">Eltávolítja az "f9c5ea4f-28f0-401a-a491-491a037fa346" azonosítójú alkalmazást a bérlői webhelyről.</span><span class="sxs-lookup"><span data-stu-id="7d9ae-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="7d9ae-116">3. példa: az alkalmazás eltávolítása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7d9ae-116">Example 3: Remove application by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="7d9ae-117">Beolvassa az alkalmazást a "b4cd1619-80b3-4cfb-9f8f-9f2333425738" azonosítójú azonosítójú objektummal, és a Remove-AzADApplication parancsmaghoz tartozó csövekkel eltávolíthatja az alkalmazást a bérlői webhelyről.</span><span class="sxs-lookup"><span data-stu-id="7d9ae-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="7d9ae-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d9ae-118">PARAMETERS</span></span>

### <span data-ttu-id="7d9ae-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7d9ae-119">-ApplicationId</span></span>
<span data-ttu-id="7d9ae-120">Az eltávolítandó alkalmazás alkalmazás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7d9ae-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="7d9ae-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d9ae-121">-DefaultProfile</span></span>
<span data-ttu-id="7d9ae-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7d9ae-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d9ae-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7d9ae-123">-DisplayName</span></span>
<span data-ttu-id="7d9ae-124">Az alkalmazás megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="7d9ae-124">The display name of the application.</span></span>

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

### <span data-ttu-id="7d9ae-125">-Force</span><span class="sxs-lookup"><span data-stu-id="7d9ae-125">-Force</span></span>
<span data-ttu-id="7d9ae-126">Ha megerősítés nélkül szeretne törölni egy alkalmazást, váltson.</span><span class="sxs-lookup"><span data-stu-id="7d9ae-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="7d9ae-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d9ae-127">-InputObject</span></span>
<span data-ttu-id="7d9ae-128">Az eltávolítandó alkalmazást jelző objektum.</span><span class="sxs-lookup"><span data-stu-id="7d9ae-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d9ae-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7d9ae-129">-ObjectId</span></span>
<span data-ttu-id="7d9ae-130">A törlendő alkalmazás objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7d9ae-130">The object id of the application to delete.</span></span>

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

### <span data-ttu-id="7d9ae-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d9ae-131">-PassThru</span></span>
<span data-ttu-id="7d9ae-132">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="7d9ae-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7d9ae-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7d9ae-133">-Confirm</span></span>
<span data-ttu-id="7d9ae-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7d9ae-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d9ae-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d9ae-135">-WhatIf</span></span>
<span data-ttu-id="7d9ae-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7d9ae-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d9ae-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7d9ae-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d9ae-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d9ae-138">CommonParameters</span></span>
<span data-ttu-id="7d9ae-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d9ae-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d9ae-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7d9ae-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d9ae-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d9ae-141">INPUTS</span></span>

### <span data-ttu-id="7d9ae-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7d9ae-142">System.String</span></span>

### <span data-ttu-id="7d9ae-143">System. GUID</span><span class="sxs-lookup"><span data-stu-id="7d9ae-143">System.Guid</span></span>

### <span data-ttu-id="7d9ae-144">Microsoft. Azure. Command. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="7d9ae-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="7d9ae-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d9ae-145">OUTPUTS</span></span>

### <span data-ttu-id="7d9ae-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7d9ae-146">System.Boolean</span></span>

## <span data-ttu-id="7d9ae-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d9ae-147">NOTES</span></span>
<span data-ttu-id="7d9ae-148">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="7d9ae-148">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="7d9ae-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d9ae-149">RELATED LINKS</span></span>

[<span data-ttu-id="7d9ae-150">Új – AzADApplication</span><span class="sxs-lookup"><span data-stu-id="7d9ae-150">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="7d9ae-151">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="7d9ae-151">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="7d9ae-152">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="7d9ae-152">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

[<span data-ttu-id="7d9ae-153">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7d9ae-153">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)
