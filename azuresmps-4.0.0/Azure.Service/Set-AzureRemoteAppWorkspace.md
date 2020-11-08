---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 608B4B5E-5DB2-4291-966C-0B25F8D4FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 18c5f50a2804aeca545c44a5c0728bf7003e9d8e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016051"
---
# <span data-ttu-id="412b1-101">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="412b1-101">Set-AzureRemoteAppWorkspace</span></span>

## <span data-ttu-id="412b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="412b1-102">SYNOPSIS</span></span>
<span data-ttu-id="412b1-103">Egy Azure RemoteApp-munkaterület tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="412b1-103">Sets the properties of an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="412b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="412b1-104">SYNTAX</span></span>

```
Set-AzureRemoteAppWorkspace [-WorkspaceName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="412b1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="412b1-105">DESCRIPTION</span></span>
<span data-ttu-id="412b1-106">A **set-AzureRemoteAppWorkspace** parancsmag az Azure RemoteApp-munkaterület tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="412b1-106">The **Set-AzureRemoteAppWorkspace** cmdlet sets the properties of an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="412b1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="412b1-107">EXAMPLES</span></span>

### <span data-ttu-id="412b1-108">Példa 1: a munkaterület nevének beállítása</span><span class="sxs-lookup"><span data-stu-id="412b1-108">Example 1: Set the workspace name</span></span>
```
PS C:\> Set-AzureRemoteAppWorkspace -WorkspaceName "Contoso Work Applications"

TrackingId
----------
12345
```

<span data-ttu-id="412b1-109">Ez a parancs beállítja az Azure RemoteApp-munkaterület nevét a contoso Work Applications alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="412b1-109">This command sets the Azure RemoteApp workspace name to Contoso Work Applications.</span></span>

## <span data-ttu-id="412b1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="412b1-110">PARAMETERS</span></span>

### <span data-ttu-id="412b1-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="412b1-111">-Profile</span></span>
<span data-ttu-id="412b1-112">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="412b1-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="412b1-113">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="412b1-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="412b1-114">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="412b1-114">-WorkspaceName</span></span>
<span data-ttu-id="412b1-115">Az Azure RemoteApp-munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="412b1-115">Specifies the name of the Azure RemoteApp workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="412b1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="412b1-116">CommonParameters</span></span>
<span data-ttu-id="412b1-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="412b1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="412b1-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="412b1-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="412b1-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="412b1-119">INPUTS</span></span>

## <span data-ttu-id="412b1-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="412b1-120">OUTPUTS</span></span>

## <span data-ttu-id="412b1-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="412b1-121">NOTES</span></span>
* <span data-ttu-id="412b1-122">A megadott előfizetéshez tartozó összes Azure RemoteApp-gyűjtemény létezik egy megosztott munkaterületen belül.</span><span class="sxs-lookup"><span data-stu-id="412b1-122">All Azure RemoteApp collections for a specified subscription exist within a shared workspace.</span></span>

## <span data-ttu-id="412b1-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="412b1-123">RELATED LINKS</span></span>

[<span data-ttu-id="412b1-124">Get-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="412b1-124">Get-AzureRemoteAppWorkspace</span></span>](./Get-AzureRemoteAppWorkspace.md)


