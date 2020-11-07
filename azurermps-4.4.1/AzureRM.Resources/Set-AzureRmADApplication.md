---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA97DB6F-F64D-417E-BD72-C2EBB2EC1AA4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
ms.openlocfilehash: 6fbbed83f9565a81b305df5cf8b66fd8210c6aec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680489"
---
# <span data-ttu-id="3c2af-101">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="3c2af-101">Set-AzureRmADApplication</span></span>

## <span data-ttu-id="3c2af-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c2af-102">SYNOPSIS</span></span>
<span data-ttu-id="3c2af-103">Frissít egy meglévő Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="3c2af-103">Updates an existing azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c2af-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c2af-104">SYNTAX</span></span>

### <span data-ttu-id="3c2af-105">ApplicationObjectIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c2af-105">ApplicationObjectIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c2af-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c2af-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ApplicationId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c2af-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c2af-107">DESCRIPTION</span></span>
<span data-ttu-id="3c2af-108">Frissít egy meglévő Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="3c2af-108">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="3c2af-109">Az alkalmazáshoz tartozó hitelesítő adatok frissítéséhez használja az New-AzureRmADAppCredential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3c2af-109">To update the credentials associated with this application, please use New-AzureRmADAppCredential cmdlet.</span></span>

## <span data-ttu-id="3c2af-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3c2af-110">EXAMPLES</span></span>

### <span data-ttu-id="3c2af-111">--------------------------Példa 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3c2af-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName" -HomePage "https://www.microsoft.com" -IdentifierUris "http://UpdatedApp" -AvailableToOtherTenants $false
```

<span data-ttu-id="3c2af-112">Egy meglévő Azure Active Directory-alkalmazás tulajdonságait frissíti a objectId "fb7b3405-CA44-4b5b-8584-12392f5d96d7" elemmel.</span><span class="sxs-lookup"><span data-stu-id="3c2af-112">Updates the properties of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

### <span data-ttu-id="3c2af-113">--------------------------Példa 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="3c2af-113">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName"
```

<span data-ttu-id="3c2af-114">Egy meglévő Azure Active Directory-alkalmazás megjelenítendő nevét frissíti a objectId "fb7b3405-CA44-4b5b-8584-12392f5d96d7" elemmel.</span><span class="sxs-lookup"><span data-stu-id="3c2af-114">Updates the display name of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

## <span data-ttu-id="3c2af-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c2af-115">PARAMETERS</span></span>

### <span data-ttu-id="3c2af-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3c2af-116">-ApplicationId</span></span>
<span data-ttu-id="3c2af-117">A frissítendő alkalmazás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3c2af-117">The id of the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c2af-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="3c2af-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="3c2af-119">Az az érték, amely meghatározza, hogy az alkalmazás frissítve lett-e egyetlen bérlői vagy többbérlői webhelyre.</span><span class="sxs-lookup"><span data-stu-id="3c2af-119">The value specifying whether the application is updated to be a single tenant or a multi-tenant.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c2af-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3c2af-120">-DisplayName</span></span>
<span data-ttu-id="3c2af-121">Az alkalmazás új megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="3c2af-121">New Display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c2af-122">-Kezdőlap</span><span class="sxs-lookup"><span data-stu-id="3c2af-122">-HomePage</span></span>
<span data-ttu-id="3c2af-123">Az alkalmazás kezdőlapjának új URL-címe.</span><span class="sxs-lookup"><span data-stu-id="3c2af-123">New URL of the application homepage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c2af-124">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="3c2af-124">-IdentifierUris</span></span>
<span data-ttu-id="3c2af-125">Az alkalmazást azonosító új URI-k.</span><span class="sxs-lookup"><span data-stu-id="3c2af-125">New URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c2af-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3c2af-126">-ObjectId</span></span>
<span data-ttu-id="3c2af-127">A frissítendő alkalmazás objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3c2af-127">The object id of the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c2af-128">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="3c2af-128">-ReplyUrls</span></span>
<span data-ttu-id="3c2af-129">Új válasz URL-címe az alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="3c2af-129">New reply urls for the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c2af-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3c2af-130">-Confirm</span></span>
<span data-ttu-id="3c2af-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3c2af-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c2af-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c2af-132">-WhatIf</span></span>
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

### <span data-ttu-id="3c2af-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c2af-133">-DefaultProfile</span></span>
<span data-ttu-id="3c2af-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c2af-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c2af-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c2af-135">CommonParameters</span></span>
<span data-ttu-id="3c2af-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c2af-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c2af-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c2af-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c2af-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c2af-138">INPUTS</span></span>

## <span data-ttu-id="3c2af-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c2af-139">OUTPUTS</span></span>

### <span data-ttu-id="3c2af-140">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="3c2af-140">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="3c2af-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c2af-141">NOTES</span></span>

## <span data-ttu-id="3c2af-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c2af-142">RELATED LINKS</span></span>

[<span data-ttu-id="3c2af-143">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="3c2af-143">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="3c2af-144">Új – AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="3c2af-144">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="3c2af-145">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="3c2af-145">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="3c2af-146">Új – AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="3c2af-146">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="3c2af-147">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="3c2af-147">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="3c2af-148">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="3c2af-148">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

