---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
ms.openlocfilehash: ea042cb0db8fcb1995a935086d188efbb6c0647f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183649"
---
# <span data-ttu-id="a47fb-101">New-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="a47fb-101">New-AzDataShareInvitation</span></span>

## <span data-ttu-id="a47fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a47fb-102">SYNOPSIS</span></span>
<span data-ttu-id="a47fb-103">Létrehoz egy megosztási meghívót.</span><span class="sxs-lookup"><span data-stu-id="a47fb-103">Creates an invitation for share.</span></span>

## <span data-ttu-id="a47fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a47fb-104">SYNTAX</span></span>

### <span data-ttu-id="a47fb-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a47fb-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareInvitation [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a47fb-106">ByInvitationEmailParameterSet</span><span class="sxs-lookup"><span data-stu-id="a47fb-106">ByInvitationEmailParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetEmail <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a47fb-107">ByInvitationTenantParameterSet</span><span class="sxs-lookup"><span data-stu-id="a47fb-107">ByInvitationTenantParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetObjectId <String> -TargetTenantId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a47fb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a47fb-108">DESCRIPTION</span></span>
<span data-ttu-id="a47fb-109">A **New-AzDataShareInvitation** parancsmag meghívót küld a célközönségnek a szolgáltatóra vonatkozó információkkal.</span><span class="sxs-lookup"><span data-stu-id="a47fb-109">The **New-AzDataShareInvitation** cmdlet sends an invitation to the target consumer with information about the provider share.</span></span> 

## <span data-ttu-id="a47fb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a47fb-110">EXAMPLES</span></span>

### <span data-ttu-id="a47fb-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a47fb-111">Example 1</span></span>
```
PS C:\> New-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation" -TargetEmail "adstest@microsoft.com"
InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/        providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="a47fb-112">Ez a parancs létrehoz egy meghívás AdsInvitation a megosztási AdsShare, és elküldi azt a cél e-mailekre adstest@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="a47fb-112">This command creates an invitation AdsInvitation for share AdsShare and sends it to target email adstest@microsoft.com.</span></span>

## <span data-ttu-id="a47fb-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a47fb-113">PARAMETERS</span></span>

### <span data-ttu-id="a47fb-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a47fb-114">-AccountName</span></span>
<span data-ttu-id="a47fb-115">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="a47fb-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a47fb-116">-DefaultProfile</span></span>
<span data-ttu-id="a47fb-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a47fb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a47fb-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a47fb-118">-Name</span></span>
<span data-ttu-id="a47fb-119">Azure Data Share meghívás neve</span><span class="sxs-lookup"><span data-stu-id="a47fb-119">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47fb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a47fb-120">-ResourceGroupName</span></span>
<span data-ttu-id="a47fb-121">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="a47fb-121">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47fb-122">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="a47fb-122">-ShareName</span></span>
<span data-ttu-id="a47fb-123">Azure-adatmegosztás neve</span><span class="sxs-lookup"><span data-stu-id="a47fb-123">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47fb-124">-TargetEmail</span><span class="sxs-lookup"><span data-stu-id="a47fb-124">-TargetEmail</span></span>
<span data-ttu-id="a47fb-125">Cél-e-mail-azonosító</span><span class="sxs-lookup"><span data-stu-id="a47fb-125">Target email id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47fb-126">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="a47fb-126">-TargetObjectId</span></span>
<span data-ttu-id="a47fb-127">Target Object ID</span><span class="sxs-lookup"><span data-stu-id="a47fb-127">Target object id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47fb-128">-TargetTenantId</span><span class="sxs-lookup"><span data-stu-id="a47fb-128">-TargetTenantId</span></span>
<span data-ttu-id="a47fb-129">Target bérlői azonosító</span><span class="sxs-lookup"><span data-stu-id="a47fb-129">Target tenant id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47fb-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a47fb-130">-Confirm</span></span>
<span data-ttu-id="a47fb-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a47fb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a47fb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a47fb-132">-WhatIf</span></span>
<span data-ttu-id="a47fb-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a47fb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a47fb-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a47fb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a47fb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a47fb-135">CommonParameters</span></span>
<span data-ttu-id="a47fb-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a47fb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a47fb-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a47fb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a47fb-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a47fb-138">INPUTS</span></span>

### <span data-ttu-id="a47fb-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="a47fb-139">None</span></span>

## <span data-ttu-id="a47fb-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a47fb-140">OUTPUTS</span></span>

### <span data-ttu-id="a47fb-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="a47fb-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="a47fb-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a47fb-142">NOTES</span></span>

## <span data-ttu-id="a47fb-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a47fb-143">RELATED LINKS</span></span>
