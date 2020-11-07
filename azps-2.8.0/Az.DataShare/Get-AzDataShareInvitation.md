---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
ms.openlocfilehash: 1f9f0258bf107ae0ca7be7050f8db8e3db8b1ffa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666737"
---
# <span data-ttu-id="09527-101">Get-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="09527-101">Get-AzDataShareInvitation</span></span>

## <span data-ttu-id="09527-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09527-102">SYNOPSIS</span></span>
<span data-ttu-id="09527-103">Meghívót kap az adatmegosztási adatokról.</span><span class="sxs-lookup"><span data-stu-id="09527-103">Gets information invitation of data share.</span></span>

## <span data-ttu-id="09527-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09527-104">SYNTAX</span></span>

### <span data-ttu-id="09527-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="09527-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09527-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09527-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareInvitation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09527-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="09527-107">DESCRIPTION</span></span>
<span data-ttu-id="09527-108">A **Get-AzDataShareInvitation** parancsmag információkat kaphat az adatmegosztásban felvett felkérésekről.</span><span class="sxs-lookup"><span data-stu-id="09527-108">The **Get-AzDataShareInvitation** cmdlet gets information on invitations added in data share.</span></span> <span data-ttu-id="09527-109">Ha megadja a meghívás nevét, ez a parancsmag információkat kap a meghívóról.</span><span class="sxs-lookup"><span data-stu-id="09527-109">If you specify the name of the invitation, this cmdlet gets information about the invitation.</span></span> <span data-ttu-id="09527-110">Ha nem ad meg nevet, ez a parancsmag információkat kap a megosztásban szereplő összes meghívóról.</span><span class="sxs-lookup"><span data-stu-id="09527-110">If you do not specify a name, this cmdlet gets information about all the invitations in a share.</span></span>

## <span data-ttu-id="09527-111">Példák</span><span class="sxs-lookup"><span data-stu-id="09527-111">EXAMPLES</span></span>

### <span data-ttu-id="09527-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="09527-112">Example 1</span></span>
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

<span data-ttu-id="09527-113">Ez a parancs információkat nyújt az adatmegosztási AdsShare lévő meghívó AdsInvitation.</span><span class="sxs-lookup"><span data-stu-id="09527-113">This commands provides information about invitation AdsInvitation present in data share AdsShare.</span></span>

## <span data-ttu-id="09527-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09527-114">PARAMETERS</span></span>

### <span data-ttu-id="09527-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="09527-115">-AccountName</span></span>
<span data-ttu-id="09527-116">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="09527-116">Azure data share account name</span></span>

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

### <span data-ttu-id="09527-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09527-117">-DefaultProfile</span></span>
<span data-ttu-id="09527-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09527-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09527-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="09527-119">-Name</span></span>
<span data-ttu-id="09527-120">Azure Data Share meghívás neve</span><span class="sxs-lookup"><span data-stu-id="09527-120">Azure data share invitation name</span></span>

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

### <span data-ttu-id="09527-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09527-121">-ResourceGroupName</span></span>
<span data-ttu-id="09527-122">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="09527-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="09527-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09527-123">-ResourceId</span></span>
<span data-ttu-id="09527-124">Az Azure-adatmegosztási meghívás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="09527-124">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="09527-125">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="09527-125">-ShareName</span></span>
<span data-ttu-id="09527-126">Azure-adatmegosztás neve</span><span class="sxs-lookup"><span data-stu-id="09527-126">Azure data share name</span></span>

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

### <span data-ttu-id="09527-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09527-127">CommonParameters</span></span>
<span data-ttu-id="09527-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09527-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09527-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09527-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09527-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09527-130">INPUTS</span></span>

### <span data-ttu-id="09527-131">System. String</span><span class="sxs-lookup"><span data-stu-id="09527-131">System.String</span></span>

## <span data-ttu-id="09527-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09527-132">OUTPUTS</span></span>

### <span data-ttu-id="09527-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="09527-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="09527-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09527-134">NOTES</span></span>

## <span data-ttu-id="09527-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09527-135">RELATED LINKS</span></span>
