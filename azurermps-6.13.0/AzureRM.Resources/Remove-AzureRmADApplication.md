---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
ms.openlocfilehash: 766b4d3bd135295cddf3dd0c143519c3dde50b0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493944"
---
# <span data-ttu-id="cc38c-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="cc38c-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="cc38c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc38c-102">SYNOPSIS</span></span>
<span data-ttu-id="cc38c-103">Törli az Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="cc38c-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc38c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc38c-104">SYNTAX</span></span>

### <span data-ttu-id="cc38c-105">ObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cc38c-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADApplication -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc38c-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc38c-106">ApplicationIdParameterSet</span></span>
```
Remove-AzureRmADApplication -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc38c-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc38c-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzureRmADApplication -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc38c-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc38c-108">InputObjectParameterSet</span></span>
```
Remove-AzureRmADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc38c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc38c-109">DESCRIPTION</span></span>
<span data-ttu-id="cc38c-110">Törli az Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="cc38c-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="cc38c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="cc38c-111">EXAMPLES</span></span>

### <span data-ttu-id="cc38c-112">Példa 1 – az alkalmazás objektum-azonosítóval való eltávolítása</span><span class="sxs-lookup"><span data-stu-id="cc38c-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="cc38c-113">Eltávolítja az "b4cd1619-80b3-4cfb-9f8f-9f2333425738" azonosítójú alkalmazást a bérlői webhelyről.</span><span class="sxs-lookup"><span data-stu-id="cc38c-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="cc38c-114">Példa 2 – alkalmazás-azonosító eltávolítása</span><span class="sxs-lookup"><span data-stu-id="cc38c-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzureRmADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="cc38c-115">Eltávolítja az "f9c5ea4f-28f0-401a-a491-491a037fa346" azonosítójú alkalmazást a bérlői webhelyről.</span><span class="sxs-lookup"><span data-stu-id="cc38c-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="cc38c-116">3 példa – alkalmazás eltávolítása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="cc38c-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzureRmADApplication
```

<span data-ttu-id="cc38c-117">Beolvassa az alkalmazást a "b4cd1619-80b3-4cfb-9f8f-9f2333425738" azonosítójú azonosítójú objektummal, és a Remove-AzureRmADApplication parancsmaghoz tartozó csövekkel eltávolíthatja az alkalmazást a bérlői webhelyről.</span><span class="sxs-lookup"><span data-stu-id="cc38c-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzureRmADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="cc38c-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc38c-118">PARAMETERS</span></span>

### <span data-ttu-id="cc38c-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="cc38c-119">-ApplicationId</span></span>
<span data-ttu-id="cc38c-120">Az eltávolítandó alkalmazás alkalmazás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cc38c-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="cc38c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc38c-121">-DefaultProfile</span></span>
<span data-ttu-id="cc38c-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cc38c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc38c-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cc38c-123">-DisplayName</span></span>
<span data-ttu-id="cc38c-124">Az alkalmazás megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="cc38c-124">The display name of the application.</span></span>

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

### <span data-ttu-id="cc38c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="cc38c-125">-Force</span></span>
<span data-ttu-id="cc38c-126">Ha megerősítés nélkül szeretne törölni egy alkalmazást, váltson.</span><span class="sxs-lookup"><span data-stu-id="cc38c-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="cc38c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc38c-127">-InputObject</span></span>
<span data-ttu-id="cc38c-128">Az eltávolítandó alkalmazást jelző objektum.</span><span class="sxs-lookup"><span data-stu-id="cc38c-128">The object representing the application to remove.</span></span>

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

### <span data-ttu-id="cc38c-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cc38c-129">-ObjectId</span></span>
<span data-ttu-id="cc38c-130">A törlendő alkalmazás objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cc38c-130">The object id of the application to delete.</span></span>

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

### <span data-ttu-id="cc38c-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc38c-131">-PassThru</span></span>
<span data-ttu-id="cc38c-132">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="cc38c-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="cc38c-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cc38c-133">-Confirm</span></span>
<span data-ttu-id="cc38c-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cc38c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc38c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc38c-135">-WhatIf</span></span>
<span data-ttu-id="cc38c-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cc38c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc38c-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc38c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc38c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc38c-138">CommonParameters</span></span>
<span data-ttu-id="cc38c-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc38c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc38c-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc38c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc38c-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc38c-141">INPUTS</span></span>

### <span data-ttu-id="cc38c-142">System. GUID</span><span class="sxs-lookup"><span data-stu-id="cc38c-142">System.Guid</span></span>

### <span data-ttu-id="cc38c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="cc38c-143">System.String</span></span>

### <span data-ttu-id="cc38c-144">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="cc38c-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="cc38c-145">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cc38c-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="cc38c-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc38c-146">OUTPUTS</span></span>

### <span data-ttu-id="cc38c-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cc38c-147">System.Boolean</span></span>

## <span data-ttu-id="cc38c-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc38c-148">NOTES</span></span>
<span data-ttu-id="cc38c-149">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="cc38c-149">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="cc38c-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc38c-150">RELATED LINKS</span></span>

[<span data-ttu-id="cc38c-151">Új – AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="cc38c-151">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="cc38c-152">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="cc38c-152">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="cc38c-153">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="cc38c-153">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="cc38c-154">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="cc38c-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

