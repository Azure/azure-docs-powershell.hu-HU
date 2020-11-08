---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 035B294E-6A1B-41E9-ACFF-D66F9C1A0B11
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9218862bb1e61abe548a94ed5297a6ce69237d54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015619"
---
# <span data-ttu-id="54098-101">Get-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="54098-101">Get-AzureRemoteAppWorkspace</span></span>

## <span data-ttu-id="54098-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54098-102">SYNOPSIS</span></span>
<span data-ttu-id="54098-103">Információt keres az Azure RemoteApp-munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="54098-103">Retrieves information about an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="54098-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54098-104">SYNTAX</span></span>

```
Get-AzureRemoteAppWorkspace [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="54098-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="54098-105">DESCRIPTION</span></span>
<span data-ttu-id="54098-106">A **Get-AzureRemoteAppWorkspace** parancsmag információkat keres az Azure RemoteApp-munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="54098-106">The **Get-AzureRemoteAppWorkspace** cmdlet retrieves information about an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="54098-107">Példák</span><span class="sxs-lookup"><span data-stu-id="54098-107">EXAMPLES</span></span>

### <span data-ttu-id="54098-108">1. példa: a munkaterület adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="54098-108">Example 1: Retrieve information about a workspace</span></span>
```
PS C:\> Get-AzureRemoteAppWorkspace
ClientUrl                               EndUserFeedName
---------                               ---------------
https://www.remoteapp.windowsazure.com/ Contoso Work Applications
```

<span data-ttu-id="54098-109">Ez a parancs információkat olvas be az Azure RemoteApp-munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="54098-109">This command retrieves information about the Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="54098-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54098-110">PARAMETERS</span></span>

### <span data-ttu-id="54098-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="54098-111">-Profile</span></span>
<span data-ttu-id="54098-112">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="54098-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54098-113">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="54098-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54098-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54098-114">CommonParameters</span></span>
<span data-ttu-id="54098-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54098-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54098-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54098-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54098-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54098-117">INPUTS</span></span>

## <span data-ttu-id="54098-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54098-118">OUTPUTS</span></span>

## <span data-ttu-id="54098-119">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54098-119">NOTES</span></span>

## <span data-ttu-id="54098-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54098-120">RELATED LINKS</span></span>

[<span data-ttu-id="54098-121">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="54098-121">Set-AzureRemoteAppWorkspace</span></span>](./Set-AzureRemoteAppWorkspace.md)


