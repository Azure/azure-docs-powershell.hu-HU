---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 636280D6-32C3-48EF-A271-A4E032F8B334
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0dab3720a4680805e16f695a1ab1b2350554e8f2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016319"
---
# <span data-ttu-id="96735-101">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="96735-101">Get-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="96735-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96735-102">SYNOPSIS</span></span>
<span data-ttu-id="96735-103">Egy vagy több közzétett Azure RemoteApp program tulajdonságainak beolvasása egy gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="96735-103">Retrieves the properties of one or more published Azure RemoteApp programs for a collection.</span></span>

## <span data-ttu-id="96735-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96735-104">SYNTAX</span></span>

### <span data-ttu-id="96735-105">FilterByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="96735-105">FilterByName (Default)</span></span>
```
Get-AzureRemoteAppProgram [-CollectionName] <String> [[-RemoteAppProgram] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="96735-106">FilterByAlias</span><span class="sxs-lookup"><span data-stu-id="96735-106">FilterByAlias</span></span>
```
Get-AzureRemoteAppProgram [-CollectionName] <String> [[-Alias] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="96735-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="96735-107">DESCRIPTION</span></span>
<span data-ttu-id="96735-108">A **Get-AzureRemoteAppProgram** parancsmag egy vagy több közzétett Azure RemoteApp program tulajdonságait keresi egy gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="96735-108">The **Get-AzureRemoteAppProgram** cmdlet retrieves the properties of one or more published Azure RemoteApp programs for a collection.</span></span>

## <span data-ttu-id="96735-109">Példák</span><span class="sxs-lookup"><span data-stu-id="96735-109">EXAMPLES</span></span>

### <span data-ttu-id="96735-110">Példa 1: a program tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="96735-110">Example 1: Retrieve the properties of a program</span></span>
```
PS C:\> Get-AzureRemoteAppProgram -CollectionName "ContosoApps" -RemoteAppProgram "Finance App"

Alias                : edc85816-4b9e-4284-b3dc-faedb505f5d9

AvailableToUsers     : True

CommandLineArguments : 

IconPngUris          : Microsoft.Azure.Management.RemoteApp.Models.IconPngUrisType

IconUri              : https://liverdcxstorage.blob.core.windows.net/icons/12345678-1234-1234-1234-123412341234.ico?se=2015-03-01T17%3A29%3A51Z&amp;amp;sr=b&amp;amp;sp=r&amp;amp;sig=abcdCCavbcF%2asY4RascaBauishCasd2FasdBHtasd2BPasdi5dasdD

Name                 : Contoso Finance

Status               : Published

VirtualPath          : %SYSTEMDRIVE%\Program Files (x86)\Contoso Finance\Finance.exe
```

<span data-ttu-id="96735-111">Ebben a parancsban egy Azure RemoteApp program tulajdonságai láthatók.</span><span class="sxs-lookup"><span data-stu-id="96735-111">This command displays the properties of an Azure RemoteApp program.</span></span>
<span data-ttu-id="96735-112">A "Penzugy" nevű program a ContosoApps nevű Azure RemoteApp-gyűjteményben található.</span><span class="sxs-lookup"><span data-stu-id="96735-112">The program, named Finance App, is in the Azure RemoteApp collection named ContosoApps.</span></span>

## <span data-ttu-id="96735-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96735-113">PARAMETERS</span></span>

### <span data-ttu-id="96735-114">-Alias</span><span class="sxs-lookup"><span data-stu-id="96735-114">-Alias</span></span>
<span data-ttu-id="96735-115">Annak a programnak az aliasát adja meg, amelynek a tulajdonságait le szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="96735-115">Specifies the alias of the program for which to retrieve properties.</span></span>

```yaml
Type: String
Parameter Sets: FilterByAlias
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96735-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="96735-116">-CollectionName</span></span>
<span data-ttu-id="96735-117">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="96735-117">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="96735-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="96735-118">-Profile</span></span>
<span data-ttu-id="96735-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="96735-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="96735-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="96735-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="96735-121">-RemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="96735-121">-RemoteAppProgram</span></span>
<span data-ttu-id="96735-122">Annak a programnak a nevét adja meg, amelynek a tulajdonságait le szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="96735-122">Specifies the name of the program for which to retrieve properties.</span></span>

```yaml
Type: String
Parameter Sets: FilterByName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="96735-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96735-123">CommonParameters</span></span>
<span data-ttu-id="96735-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96735-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96735-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96735-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96735-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96735-126">INPUTS</span></span>

## <span data-ttu-id="96735-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96735-127">OUTPUTS</span></span>

## <span data-ttu-id="96735-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96735-128">NOTES</span></span>

## <span data-ttu-id="96735-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96735-129">RELATED LINKS</span></span>

[<span data-ttu-id="96735-130">Közzététel – AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="96735-130">Publish-AzureRemoteAppProgram</span></span>](./Publish-AzureRemoteAppProgram.md)

[<span data-ttu-id="96735-131">Közzététel megszüntetése – AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="96735-131">Unpublish-AzureRemoteAppProgram</span></span>](./Unpublish-AzureRemoteAppProgram.md)


