---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: FCDEA955-EB64-4EEA-9F4A-04E2C1F0A831
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83664e8be9241782e42d7ba7634691668ed575f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016315"
---
# <span data-ttu-id="b800f-101">Get-AzureRemoteAppStartMenuProgram</span><span class="sxs-lookup"><span data-stu-id="b800f-101">Get-AzureRemoteAppStartMenuProgram</span></span>

## <span data-ttu-id="b800f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b800f-102">SYNOPSIS</span></span>
<span data-ttu-id="b800f-103">Az Azure RemoteApp-gyűjtemény Start menü programjainak listája.</span><span class="sxs-lookup"><span data-stu-id="b800f-103">Lists the Start Menu programs in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="b800f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b800f-104">SYNTAX</span></span>

```
Get-AzureRemoteAppStartMenuProgram [-CollectionName] <String> [[-ProgramName] <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b800f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b800f-105">DESCRIPTION</span></span>
<span data-ttu-id="b800f-106">A **Get-AzureRemoteAppStartMenuProgram** parancsmag az Azure RemoteApp-gyűjtemény által használt sablon képe alapján megjeleníti a Start menü programját.</span><span class="sxs-lookup"><span data-stu-id="b800f-106">The **Get-AzureRemoteAppStartMenuProgram** cmdlet lists the Start Menu programs in the template image that an Azure RemoteApp collection uses.</span></span>

## <span data-ttu-id="b800f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b800f-107">EXAMPLES</span></span>

### <span data-ttu-id="b800f-108">Példa 1: a Start menü programok listája a gyűjteményhez</span><span class="sxs-lookup"><span data-stu-id="b800f-108">Example 1: List the Start Menu programs for a collection</span></span>
```
PS C:\> Get-AzureRemoteAppStartMenuProgram -CollectionName "ContosoApps"
```

<span data-ttu-id="b800f-109">Ez a parancs a ContosoApps-gyűjtemény Start menüjének listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="b800f-109">This command returns the list of Start Menu programs for the ContosoApps collection.</span></span>

## <span data-ttu-id="b800f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b800f-110">PARAMETERS</span></span>

### <span data-ttu-id="b800f-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="b800f-111">-CollectionName</span></span>
<span data-ttu-id="b800f-112">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b800f-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b800f-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="b800f-113">-Profile</span></span>
<span data-ttu-id="b800f-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b800f-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b800f-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b800f-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b800f-116">-Programnév</span><span class="sxs-lookup"><span data-stu-id="b800f-116">-ProgramName</span></span>
<span data-ttu-id="b800f-117">Annak a programnak a nevét adja meg, amelyre vonatkozóan információkat szeretne listázni.</span><span class="sxs-lookup"><span data-stu-id="b800f-117">Specifies the name of a program for which to list information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="b800f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b800f-118">CommonParameters</span></span>
<span data-ttu-id="b800f-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b800f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b800f-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b800f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b800f-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b800f-121">INPUTS</span></span>

## <span data-ttu-id="b800f-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b800f-122">OUTPUTS</span></span>

## <span data-ttu-id="b800f-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b800f-123">NOTES</span></span>

## <span data-ttu-id="b800f-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b800f-124">RELATED LINKS</span></span>

[<span data-ttu-id="b800f-125">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="b800f-125">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)


