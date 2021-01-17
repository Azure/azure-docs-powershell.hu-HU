---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
ms.openlocfilehash: 0a723400bf92569a077abc64467c3cace56da0a6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350981"
---
# <span data-ttu-id="2e63d-101">Get-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="2e63d-101">Get-AzDataShareInvitation</span></span>

## <span data-ttu-id="2e63d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e63d-102">SYNOPSIS</span></span>
<span data-ttu-id="2e63d-103">Információmeghívást kap az adatok megosztásáról.</span><span class="sxs-lookup"><span data-stu-id="2e63d-103">Gets information invitation of data share.</span></span>

## <span data-ttu-id="2e63d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2e63d-104">SYNTAX</span></span>

### <span data-ttu-id="2e63d-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e63d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e63d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e63d-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareInvitation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e63d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2e63d-107">DESCRIPTION</span></span>
<span data-ttu-id="2e63d-108">A **Get-AzDataShareInvitation** parancsmag információkat kap az adatmegosztáshoz hozzáadott meghívókról.</span><span class="sxs-lookup"><span data-stu-id="2e63d-108">The **Get-AzDataShareInvitation** cmdlet gets information on invitations added in data share.</span></span> <span data-ttu-id="2e63d-109">Ha megadja a meghívó nevét, ez a parancsmag információt kap a meghívóról.</span><span class="sxs-lookup"><span data-stu-id="2e63d-109">If you specify the name of the invitation, this cmdlet gets information about the invitation.</span></span> <span data-ttu-id="2e63d-110">Ha nem ad meg nevet, ez a parancsmag információt kap a megosztásban található összes meghívóról.</span><span class="sxs-lookup"><span data-stu-id="2e63d-110">If you do not specify a name, this cmdlet gets information about all the invitations in a share.</span></span>

## <span data-ttu-id="2e63d-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2e63d-111">EXAMPLES</span></span>

### <span data-ttu-id="2e63d-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="2e63d-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation"

InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="2e63d-113">Ez a parancs információt nyújt a meghívó AdsInvitation funkcióról az adatmegosztási Hirdetések megosztása szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="2e63d-113">This commands provides information about invitation AdsInvitation present in data share AdsShare.</span></span>

## <span data-ttu-id="2e63d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e63d-114">PARAMETERS</span></span>

### <span data-ttu-id="2e63d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2e63d-115">-AccountName</span></span>
<span data-ttu-id="2e63d-116">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="2e63d-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e63d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e63d-117">-DefaultProfile</span></span>
<span data-ttu-id="2e63d-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e63d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e63d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2e63d-119">-Name</span></span>
<span data-ttu-id="2e63d-120">Azure-adatok megosztására szóló meghívás neve</span><span class="sxs-lookup"><span data-stu-id="2e63d-120">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e63d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e63d-121">-ResourceGroupName</span></span>
<span data-ttu-id="2e63d-122">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="2e63d-122">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e63d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e63d-123">-ResourceId</span></span>
<span data-ttu-id="2e63d-124">Az Azure-adatok megosztására szóló meghívó erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="2e63d-124">The resource id of the azure data share invitation</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e63d-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="2e63d-125">-ShareName</span></span>
<span data-ttu-id="2e63d-126">Azure-adatok megosztásának neve</span><span class="sxs-lookup"><span data-stu-id="2e63d-126">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e63d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e63d-127">CommonParameters</span></span>
<span data-ttu-id="2e63d-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e63d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e63d-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e63d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e63d-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e63d-130">INPUTS</span></span>

### <span data-ttu-id="2e63d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="2e63d-131">System.String</span></span>

## <span data-ttu-id="2e63d-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e63d-132">OUTPUTS</span></span>

### <span data-ttu-id="2e63d-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="2e63d-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="2e63d-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2e63d-134">NOTES</span></span>

## <span data-ttu-id="2e63d-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e63d-135">RELATED LINKS</span></span>
