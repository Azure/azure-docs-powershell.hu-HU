---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 1c6f6a38c1811bdda32b60d4af1707c78eb7afd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672581"
---
# <span data-ttu-id="b6a3e-101">Remove-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="b6a3e-101">Remove-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="b6a3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6a3e-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a3e-103">Törli az előfizetés biztonsági munkaterület beállítását.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-103">Deletes the security workspace setting for this subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6a3e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6a3e-104">SYNTAX</span></span>

### <span data-ttu-id="b6a3e-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b6a3e-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6a3e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6a3e-106">ResourceId</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6a3e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b6a3e-107">InputObject</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -InputObject <PSRemoveWorkspaceSettingInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6a3e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6a3e-108">DESCRIPTION</span></span>
<span data-ttu-id="b6a3e-109">Törli az előfizetés biztonsági munkaterület beállítását.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="b6a3e-110">Ezzel a műveletsorral az újonnan telepített biztonsági ügynökök jelentést tesznek a susbscription alapértelmezett munkaterületére.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-110">This action will make the newly installed security agents to report to the default workspace of this susbscription.</span></span>

## <span data-ttu-id="b6a3e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b6a3e-111">EXAMPLES</span></span>

### <span data-ttu-id="b6a3e-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b6a3e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="b6a3e-113">Törli az előfizetés biztonsági munkaterület beállítását.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="b6a3e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6a3e-114">PARAMETERS</span></span>

### <span data-ttu-id="b6a3e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a3e-115">-DefaultProfile</span></span>
<span data-ttu-id="b6a3e-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a3e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6a3e-117">-InputObject</span></span>
<span data-ttu-id="b6a3e-118">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="b6a3e-118">Input Object.</span></span>

```yaml
Type: PSRemoveWorkspaceSettingInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6a3e-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b6a3e-119">-Name</span></span>
<span data-ttu-id="b6a3e-120">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="b6a3e-120">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a3e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6a3e-121">-PassThru</span></span>
<span data-ttu-id="b6a3e-122">Adja meg, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-122">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a3e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6a3e-123">-ResourceId</span></span>
<span data-ttu-id="b6a3e-124">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-124">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6a3e-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b6a3e-125">-Confirm</span></span>
<span data-ttu-id="b6a3e-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a3e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6a3e-127">-WhatIf</span></span>
<span data-ttu-id="b6a3e-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6a3e-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a3e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a3e-130">CommonParameters</span></span>
<span data-ttu-id="b6a3e-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6a3e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a3e-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6a3e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a3e-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6a3e-133">INPUTS</span></span>

### <span data-ttu-id="b6a3e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b6a3e-134">System.String</span></span>
<span data-ttu-id="b6a3e-135">Microsoft. Azure. Command. Security. parancsmagok. WorkspaceSettings. PSRemoveWorkspaceSettingInputObject</span><span class="sxs-lookup"><span data-stu-id="b6a3e-135">Microsoft.Azure.Commands.Security.Cmdlets.WorkspaceSettings.PSRemoveWorkspaceSettingInputObject</span></span>

## <span data-ttu-id="b6a3e-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6a3e-136">OUTPUTS</span></span>

### <span data-ttu-id="b6a3e-137">Microsoft. Azure. commands. Security. models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="b6a3e-137">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="b6a3e-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6a3e-138">NOTES</span></span>

## <span data-ttu-id="b6a3e-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6a3e-139">RELATED LINKS</span></span>
