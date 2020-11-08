---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f83489d21fba97bb50145de1fedc1ac9a7195a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016184"
---
# <span data-ttu-id="b223f-101">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b223f-101">New-AzureWebsite</span></span>

## <span data-ttu-id="b223f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b223f-102">SYNOPSIS</span></span>
<span data-ttu-id="b223f-103">Az Azure-ban futtatandó új webhely létrehozása</span><span class="sxs-lookup"><span data-stu-id="b223f-103">Create a new website to run in Azure.</span></span>

## <span data-ttu-id="b223f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b223f-104">SYNTAX</span></span>

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GithubCredentials <PSCredential>] [-GithubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b223f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b223f-105">DESCRIPTION</span></span>
<span data-ttu-id="b223f-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="b223f-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b223f-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b223f-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b223f-108">A parancsmag létrehoz egy új webhelyet az Azure-ban, és előkészíti a bevezetést a githubon keresztül.</span><span class="sxs-lookup"><span data-stu-id="b223f-108">The cmdlet creates a new website to run in Azure and prepares for deployment through Github.</span></span>

## <span data-ttu-id="b223f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b223f-109">EXAMPLES</span></span>

### <span data-ttu-id="b223f-110">Példa 1: új webhely létrehozása git segítségével</span><span class="sxs-lookup"><span data-stu-id="b223f-110">Example 1: Create a new website with Git</span></span>
```
PS C:\> New-AzureWebsite mySite -Git
```

<span data-ttu-id="b223f-111">Ez a példa létrehoz egy új webhelyet az Azure-ban, és egy helyi git tárházat használ a fájlok új webhelyre történő központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="b223f-111">This example creates a new website in Azure and a local Git repository to use for deploying files to the new website.</span></span>

### <span data-ttu-id="b223f-112">2. példa: a GitHub által integrált webhely létrehozása</span><span class="sxs-lookup"><span data-stu-id="b223f-112">Example 2: Create website integrated with Github</span></span>
```
PS C:\> New-AzureWebsite mysite -Github -GithubRepository myaccount/myrepo
```

<span data-ttu-id="b223f-113">Ez a példa létrehoz egy új webhelyet, amely a MyAccount/myrepo GitHub nevű tárházához van társítva.</span><span class="sxs-lookup"><span data-stu-id="b223f-113">This example creates a new website linked to a Github repository named myaccount/myrepo.</span></span>
<span data-ttu-id="b223f-114">Kötelezettséget vállal a GitHub repositoryra az Azure-beli webhelyre.</span><span class="sxs-lookup"><span data-stu-id="b223f-114">Commits to the Github repository are pushed to the website in Azure.</span></span>

## <span data-ttu-id="b223f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b223f-115">PARAMETERS</span></span>

### <span data-ttu-id="b223f-116">-Git</span><span class="sxs-lookup"><span data-stu-id="b223f-116">-Git</span></span>
<span data-ttu-id="b223f-117">Egy helyi git repositoryt hoz létre, és a webhelyre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="b223f-117">Sets up a local Git repository and links it to the website.</span></span>
<span data-ttu-id="b223f-118">Ha meg van adva, ez a paraméter egy git-tárházat hoz létre a helyi címtárban, és felvesz egy "Azure" nevű távoli tárházat, amely az Azure webhelyére mutató hivatkozásokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b223f-118">If specified, this parameter sets up a Git repository in the local directory and add a remote repository named 'azure' that links to the website in Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b223f-119">-GitHub</span><span class="sxs-lookup"><span data-stu-id="b223f-119">-GitHub</span></span>
<span data-ttu-id="b223f-120">Jelzi, hogy ez a parancsmag az új webhelyet egy meglévő GitHub-tárházhoz csatolja.</span><span class="sxs-lookup"><span data-stu-id="b223f-120">Indicates that this cmdlet links the new website to an existing Github repository.</span></span>
<span data-ttu-id="b223f-121">A Giuthub repository véglegesítése az Azure webhelyére kerül.</span><span class="sxs-lookup"><span data-stu-id="b223f-121">Commits to the Giuthub repository are pushed to the website in Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b223f-122">-GithubCredentials</span><span class="sxs-lookup"><span data-stu-id="b223f-122">-GithubCredentials</span></span>
<span data-ttu-id="b223f-123">A Felhasználónév és a jelszó hitelesítő adatait adja meg a Githubhoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="b223f-123">Specifies the user name and password credentials to connect to Github.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b223f-124">-GithubRepository</span><span class="sxs-lookup"><span data-stu-id="b223f-124">-GithubRepository</span></span>
<span data-ttu-id="b223f-125">Itt adhatja meg a webhelyre mutató GitHub-tárház teljes nevét.</span><span class="sxs-lookup"><span data-stu-id="b223f-125">Specifies the full name of the Github repository to link to this website.</span></span>
<span data-ttu-id="b223f-126">Például: `myaccount/myrepo` .</span><span class="sxs-lookup"><span data-stu-id="b223f-126">For example, `myaccount/myrepo`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b223f-127">-Hostname (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="b223f-127">-Hostname</span></span>
<span data-ttu-id="b223f-128">Az új webhely másodlagos állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b223f-128">Specifies an alternative host name for the new website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b223f-129">-Hely</span><span class="sxs-lookup"><span data-stu-id="b223f-129">-Location</span></span>
<span data-ttu-id="b223f-130">Annak az adatközpontnak a helyét adja meg, ahol a webhelyet telepíteni szeretné.</span><span class="sxs-lookup"><span data-stu-id="b223f-130">Specifies the location of the data center where you want to deploy the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b223f-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b223f-131">-Name</span></span>
<span data-ttu-id="b223f-132">A webhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b223f-132">Specifies a name for the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b223f-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="b223f-133">-Profile</span></span>
<span data-ttu-id="b223f-134">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b223f-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b223f-135">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b223f-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b223f-136">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="b223f-136">-PublishingUsername</span></span>
<span data-ttu-id="b223f-137">Megadja, hogy milyen Felhasználónév van megadva az Azure portálon a git telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="b223f-137">Specifies the user name you have specified in the Azure Portal for Git deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b223f-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="b223f-138">-Slot</span></span>
<span data-ttu-id="b223f-139">A webhely tárolóhelyének a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b223f-139">Specifies a slot name for the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b223f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b223f-140">CommonParameters</span></span>
<span data-ttu-id="b223f-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b223f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b223f-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b223f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b223f-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b223f-143">INPUTS</span></span>

## <span data-ttu-id="b223f-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b223f-144">OUTPUTS</span></span>

## <span data-ttu-id="b223f-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b223f-145">NOTES</span></span>

## <span data-ttu-id="b223f-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b223f-146">RELATED LINKS</span></span>

[<span data-ttu-id="b223f-147">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b223f-147">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


