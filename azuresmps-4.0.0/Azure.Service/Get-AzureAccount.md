---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 70ADAF16-BC52-47BF-A85A-A84DEACDA027
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2704dbdc308b9773452b05ceba24719f2e274132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015676"
---
# <span data-ttu-id="182b9-101">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="182b9-101">Get-AzureAccount</span></span>

## <span data-ttu-id="182b9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="182b9-102">SYNOPSIS</span></span>
<span data-ttu-id="182b9-103">Az Azure PowerShellhez elérhető Azure-fiókokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="182b9-103">Gets Azure accounts that are available to Azure PowerShell.</span></span>

## <span data-ttu-id="182b9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="182b9-104">SYNTAX</span></span>

```
Get-AzureAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="182b9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="182b9-105">DESCRIPTION</span></span>
<span data-ttu-id="182b9-106">A **Get-AzureAccount** parancsmag a Windows powershellhez elérhető Azure-fiókokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="182b9-106">The **Get-AzureAccount** cmdlet gets the Azure accounts that are available to Windows PowerShell.</span></span>
<span data-ttu-id="182b9-107">Ha a fiókját elérhetővé szeretné tenni a Windows PowerShell számára, használja a **Add-AzureAccount** vagy az **import-PublishSettingsFile** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="182b9-107">To make your accounts available to Windows PowerShell, use the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlets.</span></span>

## <span data-ttu-id="182b9-108">Példák</span><span class="sxs-lookup"><span data-stu-id="182b9-108">EXAMPLES</span></span>

### <span data-ttu-id="182b9-109">Példa 1: az összes fiók lekérése</span><span class="sxs-lookup"><span data-stu-id="182b9-109">Example 1: Get all accounts</span></span>
```
PS C:\> Get-AzureAccount

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
contosotest1@outlook.com     {{ ActiveDirectoryTenantId = aaeabcde-386c-4466-bf70-794...
```

<span data-ttu-id="182b9-110">Ez a parancs beolvassa az adott felhasználóhoz társított összes fiókot.</span><span class="sxs-lookup"><span data-stu-id="182b9-110">This command gets all accounts associated with the specified user.</span></span>

### <span data-ttu-id="182b9-111">2. példa: fiók beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="182b9-111">Example 2: Get an account by name</span></span>
```
PS C:\> Get-AzureAccount -Name contosoadmin@outlook.com

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
```

<span data-ttu-id="182b9-112">Ez a parancs a ContosoAdmin-fiókot kapja.</span><span class="sxs-lookup"><span data-stu-id="182b9-112">This command gets the ContosoAdmin account.</span></span>

## <span data-ttu-id="182b9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="182b9-113">PARAMETERS</span></span>

### <span data-ttu-id="182b9-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="182b9-114">-Name</span></span>
<span data-ttu-id="182b9-115">Csak a megadott fiók kapja meg.</span><span class="sxs-lookup"><span data-stu-id="182b9-115">Gets only the specified account.</span></span>
<span data-ttu-id="182b9-116">Az alapértelmezett beállítás a Windows PowerShellhez elérhető összes fiók.</span><span class="sxs-lookup"><span data-stu-id="182b9-116">The default is all accounts that are available to Windows PowerShell.</span></span>
<span data-ttu-id="182b9-117">Írja be a fiók nevét.</span><span class="sxs-lookup"><span data-stu-id="182b9-117">Enter the account name.</span></span>
<span data-ttu-id="182b9-118">A **név** érték megkülönbözteti a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="182b9-118">The **Name** value is case-sensitive.</span></span>
<span data-ttu-id="182b9-119">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="182b9-119">Wildcards are not permitted.</span></span>

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

### <span data-ttu-id="182b9-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="182b9-120">-Profile</span></span>
<span data-ttu-id="182b9-121">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="182b9-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="182b9-122">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="182b9-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="182b9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="182b9-123">CommonParameters</span></span>
<span data-ttu-id="182b9-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="182b9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="182b9-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="182b9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="182b9-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="182b9-126">INPUTS</span></span>

### <span data-ttu-id="182b9-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="182b9-127">None</span></span>
<span data-ttu-id="182b9-128">Ebben a parancsmagban nem lehet beírni a bemenetet.</span><span class="sxs-lookup"><span data-stu-id="182b9-128">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="182b9-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="182b9-129">OUTPUTS</span></span>

### <span data-ttu-id="182b9-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="182b9-130">None</span></span>
<span data-ttu-id="182b9-131">Ez a parancsmag nem ad vissza semmilyen eredményt.</span><span class="sxs-lookup"><span data-stu-id="182b9-131">This cmdlet does not return any output.</span></span>

## <span data-ttu-id="182b9-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="182b9-132">NOTES</span></span>

## <span data-ttu-id="182b9-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="182b9-133">RELATED LINKS</span></span>

[<span data-ttu-id="182b9-134">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="182b9-134">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="182b9-135">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="182b9-135">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="182b9-136">Importálás – AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="182b9-136">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="182b9-137">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="182b9-137">Remove-AzureAccount</span></span>](./Remove-AzureAccount.md)


