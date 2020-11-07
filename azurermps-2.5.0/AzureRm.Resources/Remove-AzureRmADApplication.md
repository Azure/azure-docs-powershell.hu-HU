---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadapplication
schema: 2.0.0
ms.openlocfilehash: 73aa80f7d42a2ad29b0e5af0ae5e0e6340691733
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850222"
---
# <span data-ttu-id="15e90-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="15e90-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="15e90-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15e90-102">SYNOPSIS</span></span>
<span data-ttu-id="15e90-103">Törli az Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="15e90-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15e90-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15e90-104">SYNTAX</span></span>

### <span data-ttu-id="15e90-105">ObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="15e90-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADApplication -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15e90-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15e90-106">ApplicationIdParameterSet</span></span>
```
Remove-AzureRmADApplication -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15e90-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="15e90-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzureRmADApplication -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15e90-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15e90-108">InputObjectParameterSet</span></span>
```
Remove-AzureRmADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15e90-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="15e90-109">DESCRIPTION</span></span>
<span data-ttu-id="15e90-110">Törli az Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="15e90-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="15e90-111">Példák</span><span class="sxs-lookup"><span data-stu-id="15e90-111">EXAMPLES</span></span>

### <span data-ttu-id="15e90-112">Példa 1 – az alkalmazás objektum-azonosítóval való eltávolítása</span><span class="sxs-lookup"><span data-stu-id="15e90-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="15e90-113">Eltávolítja az "b4cd1619-80b3-4cfb-9f8f-9f2333425738" azonosítójú alkalmazást a bérlői webhelyről.</span><span class="sxs-lookup"><span data-stu-id="15e90-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="15e90-114">Példa 2 – alkalmazás-azonosító eltávolítása</span><span class="sxs-lookup"><span data-stu-id="15e90-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzureRmADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="15e90-115">Eltávolítja az "f9c5ea4f-28f0-401a-a491-491a037fa346" azonosítójú alkalmazást a bérlői webhelyről.</span><span class="sxs-lookup"><span data-stu-id="15e90-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="15e90-116">3 példa – alkalmazás eltávolítása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="15e90-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzureRmADApplication
```

<span data-ttu-id="15e90-117">Beolvassa az alkalmazást a "b4cd1619-80b3-4cfb-9f8f-9f2333425738" azonosítójú azonosítójú objektummal, és a Remove-AzureRmADApplication parancsmaghoz tartozó csövekkel eltávolíthatja az alkalmazást a bérlői webhelyről.</span><span class="sxs-lookup"><span data-stu-id="15e90-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzureRmADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="15e90-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15e90-118">PARAMETERS</span></span>

### <span data-ttu-id="15e90-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="15e90-119">-ApplicationId</span></span>
<span data-ttu-id="15e90-120">Az eltávolítandó alkalmazás alkalmazás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="15e90-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="15e90-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15e90-121">-DefaultProfile</span></span>
<span data-ttu-id="15e90-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="15e90-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15e90-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="15e90-123">-DisplayName</span></span>
<span data-ttu-id="15e90-124">Az alkalmazás megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="15e90-124">The display name of the application.</span></span>

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

### <span data-ttu-id="15e90-125">-Force</span><span class="sxs-lookup"><span data-stu-id="15e90-125">-Force</span></span>
<span data-ttu-id="15e90-126">Ha megerősítés nélkül szeretne törölni egy alkalmazást, váltson.</span><span class="sxs-lookup"><span data-stu-id="15e90-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="15e90-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15e90-127">-InputObject</span></span>
<span data-ttu-id="15e90-128">Az eltávolítandó alkalmazást jelző objektum.</span><span class="sxs-lookup"><span data-stu-id="15e90-128">The object representing the application to remove.</span></span>

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

### <span data-ttu-id="15e90-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="15e90-129">-ObjectId</span></span>
<span data-ttu-id="15e90-130">A törlendő alkalmazás objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="15e90-130">The object id of the application to delete.</span></span>

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

### <span data-ttu-id="15e90-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15e90-131">-PassThru</span></span>
<span data-ttu-id="15e90-132">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="15e90-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="15e90-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="15e90-133">-Confirm</span></span>
<span data-ttu-id="15e90-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="15e90-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15e90-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15e90-135">-WhatIf</span></span>
<span data-ttu-id="15e90-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="15e90-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15e90-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="15e90-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15e90-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15e90-138">CommonParameters</span></span>
<span data-ttu-id="15e90-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15e90-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15e90-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15e90-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15e90-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15e90-141">INPUTS</span></span>

### <span data-ttu-id="15e90-142">System. GUID</span><span class="sxs-lookup"><span data-stu-id="15e90-142">System.Guid</span></span>

### <span data-ttu-id="15e90-143">System. String</span><span class="sxs-lookup"><span data-stu-id="15e90-143">System.String</span></span>

### <span data-ttu-id="15e90-144">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="15e90-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="15e90-145">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="15e90-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="15e90-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15e90-146">OUTPUTS</span></span>

### <span data-ttu-id="15e90-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="15e90-147">System.Boolean</span></span>

## <span data-ttu-id="15e90-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15e90-148">NOTES</span></span>
<span data-ttu-id="15e90-149">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="15e90-149">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="15e90-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15e90-150">RELATED LINKS</span></span>

[<span data-ttu-id="15e90-151">Új – AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="15e90-151">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="15e90-152">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="15e90-152">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)



[<span data-ttu-id="15e90-153">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="15e90-153">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

