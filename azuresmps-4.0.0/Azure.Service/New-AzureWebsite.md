---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 768eff2dda32c6dfa0bad14f028338d3c5fa1abd
ms.sourcegitcommit: 87730c7ea4f98f628d3fe1b40aa4a9d2885e1c75
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/12/2021
ms.locfileid: "98110478"
---
# <span data-ttu-id="ca9d8-101">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ca9d8-101">New-AzureWebsite</span></span>

## <span data-ttu-id="ca9d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca9d8-102">SYNOPSIS</span></span>
<span data-ttu-id="ca9d8-103">Hozzon létre egy új webhelyet az Azure-ban való futtatáshoz.</span><span class="sxs-lookup"><span data-stu-id="ca9d8-103">Create a new website to run in Azure.</span></span>

## <span data-ttu-id="ca9d8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ca9d8-104">SYNTAX</span></span>

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GitHubCredentials <PSCredential>] [-GitHubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ca9d8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ca9d8-105">DESCRIPTION</span></span>
<span data-ttu-id="ca9d8-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10-es verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="ca9d8-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ca9d8-107">A használt modul verziójának lekérte az Azure PowerShell konzolban a `(Get-Module -Name Azure).Version` következőt: .</span><span class="sxs-lookup"><span data-stu-id="ca9d8-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ca9d8-108">A parancsmag létrehoz egy új webhelyet az Azure-ban való futtatáshoz, és felkészül a GitHubon keresztüli telepítésre.</span><span class="sxs-lookup"><span data-stu-id="ca9d8-108">The cmdlet creates a new website to run in Azure and prepares for deployment through GitHub.</span></span>

## <span data-ttu-id="ca9d8-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ca9d8-109">EXAMPLES</span></span>

### <span data-ttu-id="ca9d8-110">1. példa: Új webhely létrehozása a Git segítségével</span><span class="sxs-lookup"><span data-stu-id="ca9d8-110">Example 1: Create a new website with Git</span></span>
```
PS C:\> New-AzureWebsite mySite -Git
```

<span data-ttu-id="ca9d8-111">Ebben a példában egy új webhelyet hoz létre az Azure-ban, és egy helyi Git-tárházat, használhatja a fájlok új webhelyre való telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="ca9d8-111">This example creates a new website in Azure and a local Git repository to use for deploying files to the new website.</span></span>

### <span data-ttu-id="ca9d8-112">2. példa: Webhely létrehozása a GitHubbal integrálva</span><span class="sxs-lookup"><span data-stu-id="ca9d8-112">Example 2: Create website integrated with GitHub</span></span>
```
PS C:\> New-AzureWebsite mysite -GitHub -GitHubRepository myaccount/myrepo
```

<span data-ttu-id="ca9d8-113">Ez a példa létrehoz egy új webhelyet, amely egy Myaccount/myrepo nevű GitHub-tárházhoz van csatolva.</span><span class="sxs-lookup"><span data-stu-id="ca9d8-113">This example creates a new website linked to a GitHub repository named myaccount/myrepo.</span></span>
<span data-ttu-id="ca9d8-114">A GitHub-tárházba való kötelezettséget a rendszer az Azure-ban a webhelyre tetszetzi.</span><span class="sxs-lookup"><span data-stu-id="ca9d8-114">Commits to the GitHub repository are pushed to the website in Azure.</span></span>

## <span data-ttu-id="ca9d8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca9d8-115">PARAMETERS</span></span>

### <span data-ttu-id="ca9d8-116">-Git</span><span class="sxs-lookup"><span data-stu-id="ca9d8-116">-Git</span></span>
<span data-ttu-id="ca9d8-117">Beállítja a helyi Git-tárat, és a webhelyre mutató hivatkozást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ca9d8-117">Sets up a local Git repository and links it to the website.</span></span>
<span data-ttu-id="ca9d8-118">Ha meg van adva, ez a paraméter beállítja a Git-tárat a helyi címtárban, és hozzáad egy "azure" nevű távoli tárat, amely az Azure-beli webhelyre mutató hivatkozást tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="ca9d8-118">If specified, this parameter sets up a Git repository in the local directory and add a remote repository named 'azure' that links to the website in Azure.</span></span>

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

### <span data-ttu-id="ca9d8-119">-GitHub</span><span class="sxs-lookup"><span data-stu-id="ca9d8-119">-GitHub</span></span>
<span data-ttu-id="ca9d8-120">Azt jelzi, hogy ez a parancsmag egy meglévő GitHub-tárházhoz kapcsolódik az új webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="ca9d8-120">Indicates that this cmdlet links the new website to an existing GitHub repository.</span></span>
<span data-ttu-id="ca9d8-121">A Giuthub-tárházba való kötelezettséget a rendszer az Azure-ban a webhelyre tolta.</span><span class="sxs-lookup"><span data-stu-id="ca9d8-121">Commits to the Giuthub repository are pushed to the website in Azure.</span></span>

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

### <span data-ttu-id="ca9d8-122">-GitHubCredentials</span><span class="sxs-lookup"><span data-stu-id="ca9d8-122">-GitHubCredentials</span></span>
<span data-ttu-id="ca9d8-123">A GitHubhoz való csatlakozáshoz használt felhasználónév és jelszó hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca9d8-123">Specifies the user name and password credentials to connect to GitHub.</span></span>

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

### <span data-ttu-id="ca9d8-124">-GitHubRepository</span><span class="sxs-lookup"><span data-stu-id="ca9d8-124">-GitHubRepository</span></span>
<span data-ttu-id="ca9d8-125">A webhelyre mutató hivatkozás gitHub-tár teljes nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca9d8-125">Specifies the full name of the GitHub repository to link to this website.</span></span>
<span data-ttu-id="ca9d8-126">`myaccount/myrepo`Például.</span><span class="sxs-lookup"><span data-stu-id="ca9d8-126">For example, `myaccount/myrepo`.</span></span>

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

### <span data-ttu-id="ca9d8-127">-Hostname</span><span class="sxs-lookup"><span data-stu-id="ca9d8-127">-Hostname</span></span>
<span data-ttu-id="ca9d8-128">Az új webhely alternatív állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca9d8-128">Specifies an alternative host name for the new website.</span></span>

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

### <span data-ttu-id="ca9d8-129">-Location</span><span class="sxs-lookup"><span data-stu-id="ca9d8-129">-Location</span></span>
<span data-ttu-id="ca9d8-130">Megadja annak az adatközpontnak a helyét, ahová a webhelyet telepíteni szeretné.</span><span class="sxs-lookup"><span data-stu-id="ca9d8-130">Specifies the location of the data center where you want to deploy the website.</span></span>

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

### <span data-ttu-id="ca9d8-131">-Name</span><span class="sxs-lookup"><span data-stu-id="ca9d8-131">-Name</span></span>
<span data-ttu-id="ca9d8-132">Megadja a webhely nevét.</span><span class="sxs-lookup"><span data-stu-id="ca9d8-132">Specifies a name for the website.</span></span>

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

### <span data-ttu-id="ca9d8-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="ca9d8-133">-Profile</span></span>
<span data-ttu-id="ca9d8-134">Azt az Azure-profilt adja meg, amelyből a parancsmag olvas.</span><span class="sxs-lookup"><span data-stu-id="ca9d8-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ca9d8-135">Ha nem ad meg profilt, ez a parancsmag a helyi alapértelmezett profilból olvassa be.</span><span class="sxs-lookup"><span data-stu-id="ca9d8-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ca9d8-136">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="ca9d8-136">-PublishingUsername</span></span>
<span data-ttu-id="ca9d8-137">Az Azure Portal for Git-telepítésben megadott felhasználónevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca9d8-137">Specifies the user name you have specified in the Azure Portal for Git deployment.</span></span>

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

### <span data-ttu-id="ca9d8-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="ca9d8-138">-Slot</span></span>
<span data-ttu-id="ca9d8-139">Megadja a webhely helynevét.</span><span class="sxs-lookup"><span data-stu-id="ca9d8-139">Specifies a slot name for the website.</span></span>

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

### <span data-ttu-id="ca9d8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca9d8-140">CommonParameters</span></span>
<span data-ttu-id="ca9d8-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca9d8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca9d8-142">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca9d8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca9d8-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca9d8-143">INPUTS</span></span>

## <span data-ttu-id="ca9d8-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca9d8-144">OUTPUTS</span></span>

## <span data-ttu-id="ca9d8-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ca9d8-145">NOTES</span></span>

## <span data-ttu-id="ca9d8-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca9d8-146">RELATED LINKS</span></span>

[<span data-ttu-id="ca9d8-147">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ca9d8-147">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


