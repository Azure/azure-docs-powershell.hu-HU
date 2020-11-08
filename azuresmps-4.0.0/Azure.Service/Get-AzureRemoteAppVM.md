---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D40937C2-9BF7-4371-A64C-B44F5B6B895E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c9882e805504b2e3b2e4f4ebbe661268b2327a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016571"
---
# <span data-ttu-id="66242-101">Get-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="66242-101">Get-AzureRemoteAppVM</span></span>

## <span data-ttu-id="66242-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66242-102">SYNOPSIS</span></span>
<span data-ttu-id="66242-103">Az Azure RemoteApp-gyűjteményben a virtuális gépeket kapja.</span><span class="sxs-lookup"><span data-stu-id="66242-103">Gets the virtual machines in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="66242-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66242-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVM -CollectionName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="66242-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="66242-105">DESCRIPTION</span></span>
<span data-ttu-id="66242-106">A **Get-AzureRemoteAppVM** parancsmag az Azure RemoteApp-gyűjtemény keretében létrehozott virtuális gépeket kapja meg a munkamenetek üzemeltetéséhez.</span><span class="sxs-lookup"><span data-stu-id="66242-106">The **Get-AzureRemoteAppVM** cmdlet gets the virtual machines created under an Azure RemoteApp collection for session hosting.</span></span>

## <span data-ttu-id="66242-107">Példák</span><span class="sxs-lookup"><span data-stu-id="66242-107">EXAMPLES</span></span>

### <span data-ttu-id="66242-108">Példa 1: a virtuális gépek megjelenítése egy gyűjteményben</span><span class="sxs-lookup"><span data-stu-id="66242-108">Example 1: Display the virtual machines in a collection</span></span>
```
PS C:\> Get-AzureRemoteAppVM -CollectionName "Contoso"
```

<span data-ttu-id="66242-109">Ez a parancs megjeleníti a contoso nevű Azure RemoteApp-gyűjteményben a munkamenetek üzemeltetéséhez használt virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="66242-109">This command displays the virtual machines used for session hosting in an Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="66242-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66242-110">PARAMETERS</span></span>

### <span data-ttu-id="66242-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="66242-111">-CollectionName</span></span>
<span data-ttu-id="66242-112">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="66242-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66242-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="66242-113">-Profile</span></span>
<span data-ttu-id="66242-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="66242-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="66242-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="66242-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="66242-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66242-116">CommonParameters</span></span>
<span data-ttu-id="66242-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66242-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66242-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66242-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66242-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66242-119">INPUTS</span></span>

## <span data-ttu-id="66242-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66242-120">OUTPUTS</span></span>

## <span data-ttu-id="66242-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66242-121">NOTES</span></span>

## <span data-ttu-id="66242-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66242-122">RELATED LINKS</span></span>

[<span data-ttu-id="66242-123">Újraindítás – AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="66242-123">Restart-AzureRemoteAppVM</span></span>](./Restart-AzureRemoteAppVM.md)


