---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 70bfdb4f590c855199bb8bbd14db4e92809b48f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845201"
---
# <span data-ttu-id="76193-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="76193-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="76193-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76193-102">SYNOPSIS</span></span>
<span data-ttu-id="76193-103">Új Azure NetApp-fájlokat (ANF) tartalmazó fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="76193-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="76193-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76193-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76193-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="76193-105">DESCRIPTION</span></span>
<span data-ttu-id="76193-106">A **New-AzNetAppFilesAccount** parancsmag létrehoz egy ANF-fiókot.</span><span class="sxs-lookup"><span data-stu-id="76193-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="76193-107">Példák</span><span class="sxs-lookup"><span data-stu-id="76193-107">EXAMPLES</span></span>

### <span data-ttu-id="76193-108">1. példa: ANF-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="76193-108">Example 1: Create an ANF account</span></span>
```
PS C:\>New-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount" -l "westus2"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="76193-109">Ezzel a paranccsal létrejön az új ANF-fiók "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="76193-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="76193-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76193-110">PARAMETERS</span></span>

### <span data-ttu-id="76193-111">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="76193-111">-ActiveDirectories</span></span>
<span data-ttu-id="76193-112">Az aktív könyvtárakat reprezentáló Hashtable tömb</span><span class="sxs-lookup"><span data-stu-id="76193-112">A hashtable array which represents the active directories</span></span>

```yaml
Type: PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76193-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76193-113">-DefaultProfile</span></span>
<span data-ttu-id="76193-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76193-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76193-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="76193-115">-Location</span></span>
<span data-ttu-id="76193-116">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="76193-116">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76193-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="76193-117">-Name</span></span>
<span data-ttu-id="76193-118">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="76193-118">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76193-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76193-119">-ResourceGroupName</span></span>
<span data-ttu-id="76193-120">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="76193-120">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76193-121">-Címke</span><span class="sxs-lookup"><span data-stu-id="76193-121">-Tag</span></span>
<span data-ttu-id="76193-122">Egy Hashtable, amely az erőforrás címkéit képviseli</span><span class="sxs-lookup"><span data-stu-id="76193-122">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76193-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="76193-123">-Confirm</span></span>
<span data-ttu-id="76193-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="76193-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76193-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76193-125">-WhatIf</span></span>
<span data-ttu-id="76193-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="76193-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76193-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="76193-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76193-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76193-128">CommonParameters</span></span>
<span data-ttu-id="76193-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76193-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="76193-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76193-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76193-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76193-131">INPUTS</span></span>

### <span data-ttu-id="76193-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="76193-132">None</span></span>

## <span data-ttu-id="76193-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76193-133">OUTPUTS</span></span>

### <span data-ttu-id="76193-134">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="76193-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="76193-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76193-135">NOTES</span></span>

## <span data-ttu-id="76193-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76193-136">RELATED LINKS</span></span>
