---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F101382E-B015-4913-B4A0-8827EC423319
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37c4bf3ad2c2aaf74f268b18d17b6af71f4f2fc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015884"
---
# <span data-ttu-id="d31c9-101">Publish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="d31c9-101">Publish-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="d31c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d31c9-102">SYNOPSIS</span></span>
<span data-ttu-id="d31c9-103">Az Azure RemoteApp program közzététele.</span><span class="sxs-lookup"><span data-stu-id="d31c9-103">Publishes an Azure RemoteApp program.</span></span>

## <span data-ttu-id="d31c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d31c9-104">SYNTAX</span></span>

### <span data-ttu-id="d31c9-105">App-azonosító (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d31c9-105">App Id (Default)</span></span>
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-StartMenuAppId] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d31c9-106">Az App elérési útja</span><span class="sxs-lookup"><span data-stu-id="d31c9-106">App Path</span></span>
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-FileVirtualPath] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d31c9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d31c9-107">DESCRIPTION</span></span>
<span data-ttu-id="d31c9-108">A **Közzététel-AzureRemoteAppProgram** parancsmag egy Azure RemoteApp programot tesz közzé, amely az Azure RemoteApp gyűjtemény felhasználói számára elérhetővé teszi az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="d31c9-108">The **Publish-AzureRemoteAppProgram** cmdlet publishes an Azure RemoteApp program, which makes it available to users of the Azure RemoteApp collection.</span></span>

## <span data-ttu-id="d31c9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d31c9-109">EXAMPLES</span></span>

### <span data-ttu-id="d31c9-110">Példa 1: program közzététele egy gyűjteményben</span><span class="sxs-lookup"><span data-stu-id="d31c9-110">Example 1: Publish a program in a collection</span></span>
```
PS C:\> Publish-AzureRemoteAppProgram -CollectionName "ContosoApps" -StartMenuAppId "a3732322-89a5-4cbc-9844-9634c74d337f" -DisplayName "Finance App"
```

<span data-ttu-id="d31c9-111">Ez a parancs közzéteszi a programot az ContosoApps-gyűjteményben a megadott *StartMenuAppId* a program a Start menübe való felvételéhez.</span><span class="sxs-lookup"><span data-stu-id="d31c9-111">This command publishes the program in the ContosoApps collection with the specified *StartMenuAppId* to add the program to the Start Menu.</span></span>
<span data-ttu-id="d31c9-112">A közzétett alkalmazás a "Penzugy app" megjelenítendő nevét fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="d31c9-112">The published app will have a display name of "Finance App".</span></span>

## <span data-ttu-id="d31c9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d31c9-113">PARAMETERS</span></span>

### <span data-ttu-id="d31c9-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="d31c9-114">-CollectionName</span></span>
<span data-ttu-id="d31c9-115">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d31c9-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="d31c9-116">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="d31c9-116">-CommandLine</span></span>
<span data-ttu-id="d31c9-117">A parancsmag által közzétett program parancssori argumentumait adja meg.</span><span class="sxs-lookup"><span data-stu-id="d31c9-117">Specifies command-line arguments for the program that this cmdlet publishes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d31c9-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d31c9-118">-DisplayName</span></span>
<span data-ttu-id="d31c9-119">Az Azure RemoteApp program felhasználóbarát megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d31c9-119">Specifies the user-friendly display name of the Azure RemoteApp program.</span></span>
<span data-ttu-id="d31c9-120">A felhasználók ezt az alkalmazás nevét látják.</span><span class="sxs-lookup"><span data-stu-id="d31c9-120">Users see this as the name of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d31c9-121">-FileVirtualPath</span><span class="sxs-lookup"><span data-stu-id="d31c9-121">-FileVirtualPath</span></span>
<span data-ttu-id="d31c9-122">Megadja a program elérési útját a program sablon képén belül.</span><span class="sxs-lookup"><span data-stu-id="d31c9-122">Specifies the path of the program within the template image of the program.</span></span>

```yaml
Type: String
Parameter Sets: App Path
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d31c9-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="d31c9-123">-Profile</span></span>
<span data-ttu-id="d31c9-124">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d31c9-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d31c9-125">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d31c9-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d31c9-126">-StartMenuAppId</span><span class="sxs-lookup"><span data-stu-id="d31c9-126">-StartMenuAppId</span></span>
<span data-ttu-id="d31c9-127">Azt a globálisan egyedi azonosítót adja meg, amely a parancsmag által a programnak a Start menübe való felvételéhez használható.</span><span class="sxs-lookup"><span data-stu-id="d31c9-127">Specifies a GUID that this cmdlet uses to add the program to the Start Menu.</span></span>

```yaml
Type: String
Parameter Sets: App Id
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d31c9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d31c9-128">CommonParameters</span></span>
<span data-ttu-id="d31c9-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d31c9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d31c9-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d31c9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d31c9-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d31c9-131">INPUTS</span></span>

## <span data-ttu-id="d31c9-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d31c9-132">OUTPUTS</span></span>

## <span data-ttu-id="d31c9-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d31c9-133">NOTES</span></span>

## <span data-ttu-id="d31c9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d31c9-134">RELATED LINKS</span></span>

[<span data-ttu-id="d31c9-135">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="d31c9-135">Get-AzureRemoteAppProgram</span></span>](./Get-AzureRemoteAppProgram.md)

[<span data-ttu-id="d31c9-136">Közzététel megszüntetése – AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="d31c9-136">Unpublish-AzureRemoteAppProgram</span></span>](./Unpublish-AzureRemoteAppProgram.md)


