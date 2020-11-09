---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 939b50f6725497bb28ea333f13c04c6281f34611
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297533"
---
# <span data-ttu-id="8073b-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="8073b-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="8073b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8073b-102">SYNOPSIS</span></span>
<span data-ttu-id="8073b-103">Információt kap a fogyasztói meghívásokról.</span><span class="sxs-lookup"><span data-stu-id="8073b-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="8073b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8073b-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8073b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8073b-105">DESCRIPTION</span></span>
<span data-ttu-id="8073b-106">A **Get-AzDataShareReceivedInvitation** parancsmag információkat nyújt a fogyasztó által receieved összes meghívóról.</span><span class="sxs-lookup"><span data-stu-id="8073b-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="8073b-107">Ha hely-vagy felkérés-azonosítót ad meg, ez a parancsmag információkat nyújt a meghívásról vagy a meghívás azonosítóról. Ellenkező esetben a fogyasztónak küldött meghívások listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8073b-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="8073b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8073b-108">EXAMPLES</span></span>

### <span data-ttu-id="8073b-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8073b-109">Example 1</span></span>
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

<span data-ttu-id="8073b-110">Ez a témakör a fogyasztói meghívásokról nyújt tájékoztatást.</span><span class="sxs-lookup"><span data-stu-id="8073b-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="8073b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8073b-111">PARAMETERS</span></span>

### <span data-ttu-id="8073b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8073b-112">-DefaultProfile</span></span>
<span data-ttu-id="8073b-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8073b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8073b-114">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="8073b-114">-InvitationId</span></span>
<span data-ttu-id="8073b-115">Azure dataShare meghívás azonosítója</span><span class="sxs-lookup"><span data-stu-id="8073b-115">Azure dataShare invitation id.</span></span>

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

### <span data-ttu-id="8073b-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="8073b-116">-Location</span></span>
<span data-ttu-id="8073b-117">Azure adatmegosztási meghívás helye.</span><span class="sxs-lookup"><span data-stu-id="8073b-117">Azure data share invitation location.</span></span>

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

### <span data-ttu-id="8073b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8073b-118">CommonParameters</span></span>
<span data-ttu-id="8073b-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8073b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8073b-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8073b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8073b-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8073b-121">INPUTS</span></span>

### <span data-ttu-id="8073b-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="8073b-122">None</span></span>

## <span data-ttu-id="8073b-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8073b-123">OUTPUTS</span></span>

### <span data-ttu-id="8073b-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="8073b-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="8073b-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8073b-125">NOTES</span></span>

## <span data-ttu-id="8073b-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8073b-126">RELATED LINKS</span></span>
