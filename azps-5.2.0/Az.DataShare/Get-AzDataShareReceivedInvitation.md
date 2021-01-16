---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 939b50f6725497bb28ea333f13c04c6281f34611
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372300"
---
# <span data-ttu-id="c5686-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="c5686-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="c5686-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5686-102">SYNOPSIS</span></span>
<span data-ttu-id="c5686-103">Információkat kap a fogyasztói meghívókról.</span><span class="sxs-lookup"><span data-stu-id="c5686-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="c5686-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c5686-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5686-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c5686-105">DESCRIPTION</span></span>
<span data-ttu-id="c5686-106">A **Get-AzDataShareReceivedInvitation** parancsmag információt nyújt a felhasználó által visszavont összes meghívásról.</span><span class="sxs-lookup"><span data-stu-id="c5686-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="c5686-107">Ha hely- vagy meghívóazonosítót ad meg, ez a parancsmag adott helyen szolgáltat információkat a meghívásról vagy a meghívóazonosítóról. Ellenkező esetben a felhasználónak küldött meghívók listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c5686-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="c5686-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c5686-108">EXAMPLES</span></span>

### <span data-ttu-id="c5686-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="c5686-109">Example 1</span></span>
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

<span data-ttu-id="c5686-110">Ez a commant információkat nyújt a fogyasztói meghívókról.</span><span class="sxs-lookup"><span data-stu-id="c5686-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="c5686-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5686-111">PARAMETERS</span></span>

### <span data-ttu-id="c5686-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5686-112">-DefaultProfile</span></span>
<span data-ttu-id="c5686-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5686-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5686-114">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="c5686-114">-InvitationId</span></span>
<span data-ttu-id="c5686-115">Azure DataShare meghívóazonosító.</span><span class="sxs-lookup"><span data-stu-id="c5686-115">Azure dataShare invitation id.</span></span>

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

### <span data-ttu-id="c5686-116">-Location</span><span class="sxs-lookup"><span data-stu-id="c5686-116">-Location</span></span>
<span data-ttu-id="c5686-117">Az Azure-adatok megosztására vonatkozó meghívás helye.</span><span class="sxs-lookup"><span data-stu-id="c5686-117">Azure data share invitation location.</span></span>

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

### <span data-ttu-id="c5686-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5686-118">CommonParameters</span></span>
<span data-ttu-id="c5686-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5686-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5686-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5686-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5686-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5686-121">INPUTS</span></span>

### <span data-ttu-id="c5686-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="c5686-122">None</span></span>

## <span data-ttu-id="c5686-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5686-123">OUTPUTS</span></span>

### <span data-ttu-id="c5686-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="c5686-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="c5686-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c5686-125">NOTES</span></span>

## <span data-ttu-id="c5686-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5686-126">RELATED LINKS</span></span>
