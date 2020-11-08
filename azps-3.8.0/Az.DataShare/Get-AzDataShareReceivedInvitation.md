---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 18cd37f1e24851720299a647a30323f9379bea6a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011169"
---
# <span data-ttu-id="9bd6b-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="9bd6b-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="9bd6b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9bd6b-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd6b-103">Információt kap a fogyasztói meghívásokról.</span><span class="sxs-lookup"><span data-stu-id="9bd6b-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="9bd6b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9bd6b-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bd6b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9bd6b-105">DESCRIPTION</span></span>
<span data-ttu-id="9bd6b-106">A **Get-AzDataShareReceivedInvitation** parancsmag információkat nyújt a fogyasztó által receieved összes meghívóról.</span><span class="sxs-lookup"><span data-stu-id="9bd6b-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="9bd6b-107">Ha hely-vagy felkérés-azonosítót ad meg, ez a parancsmag információkat nyújt a meghívásról vagy a meghívás azonosítóról. Ellenkező esetben a fogyasztónak küldött meghívások listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9bd6b-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="9bd6b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="9bd6b-108">EXAMPLES</span></span>

### <span data-ttu-id="9bd6b-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9bd6b-109">Example 1</span></span>
```
PS C:\> Get-AzDataShareReceivedInvitation -location "westus"

DataSetCount      : 3
InvitationId      : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus  : Pending
Location          : westus
RespondedAt       :
Sender            : adsprovider@microsoft.com
SenderCompanyName : ADS Test
SentAt            : 7/8/2019 10:47:10 PM
ShareName         : AdsShare
Description       : Some description
Terms             : Some terms of use
Id                : /providers/Microsoft.DataShare/consumerInvitations/167e06ff-567f-4bc7-be0c-645a6de710f3
Name              : AdsInvitation
Type              : Microsoft.DataShare/consumerInvitations
```

<span data-ttu-id="9bd6b-110">Ez a témakör a fogyasztói meghívásokról nyújt tájékoztatást.</span><span class="sxs-lookup"><span data-stu-id="9bd6b-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="9bd6b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9bd6b-111">PARAMETERS</span></span>

### <span data-ttu-id="9bd6b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd6b-112">-DefaultProfile</span></span>
<span data-ttu-id="9bd6b-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9bd6b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bd6b-114">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="9bd6b-114">-InvitationId</span></span>
<span data-ttu-id="9bd6b-115">Azure dataShare meghívás azonosítója</span><span class="sxs-lookup"><span data-stu-id="9bd6b-115">Azure dataShare invitation id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd6b-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="9bd6b-116">-Location</span></span>
<span data-ttu-id="9bd6b-117">Azure adatmegosztási meghívás helye.</span><span class="sxs-lookup"><span data-stu-id="9bd6b-117">Azure data share invitation location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd6b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd6b-118">CommonParameters</span></span>
<span data-ttu-id="9bd6b-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9bd6b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd6b-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bd6b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd6b-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bd6b-121">INPUTS</span></span>

### <span data-ttu-id="9bd6b-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="9bd6b-122">None</span></span>

## <span data-ttu-id="9bd6b-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bd6b-123">OUTPUTS</span></span>

### <span data-ttu-id="9bd6b-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="9bd6b-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="9bd6b-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9bd6b-125">NOTES</span></span>

## <span data-ttu-id="9bd6b-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9bd6b-126">RELATED LINKS</span></span>
