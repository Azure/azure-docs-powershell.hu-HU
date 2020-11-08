---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 3bb602d148b0843def129a1e4538d9ef8fdbe169
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184259"
---
# <span data-ttu-id="56cc3-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="56cc3-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="56cc3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="56cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="56cc3-103">Új helyreállítási szolgáltatások boltozatának létrehozása</span><span class="sxs-lookup"><span data-stu-id="56cc3-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="56cc3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="56cc3-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56cc3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="56cc3-105">DESCRIPTION</span></span>
<span data-ttu-id="56cc3-106">A **New-AzRecoveryServicesVault** parancsmag új helyreállítási szolgáltatások boltozatát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="56cc3-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="56cc3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="56cc3-107">EXAMPLES</span></span>

### <span data-ttu-id="56cc3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="56cc3-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="56cc3-109">Helyreállítási szolgáltatás boltozatának létrehozása az erőforrás csoportban és az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="56cc3-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="56cc3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="56cc3-110">PARAMETERS</span></span>

### <span data-ttu-id="56cc3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56cc3-111">-DefaultProfile</span></span>
<span data-ttu-id="56cc3-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="56cc3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56cc3-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="56cc3-113">-Location</span></span>
<span data-ttu-id="56cc3-114">A boltozat földrajzi helyének a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="56cc3-114">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56cc3-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="56cc3-115">-Name</span></span>
<span data-ttu-id="56cc3-116">A létrehozandó boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="56cc3-116">Specifies the name of the vault to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56cc3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56cc3-117">-ResourceGroupName</span></span>
<span data-ttu-id="56cc3-118">Annak az Azure-erőforrás csoportnak a nevét adja meg, amelyből a megadott helyreállítási szolgáltatások objektumát szeretné létrehozni vagy onnan beolvasni.</span><span class="sxs-lookup"><span data-stu-id="56cc3-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56cc3-119">-Címke</span><span class="sxs-lookup"><span data-stu-id="56cc3-119">-Tag</span></span>

<span data-ttu-id="56cc3-120">A helyreállítási szolgáltatások Boltozatához hozzáadni kívánt címkéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="56cc3-120">Specifies the Tags to add to the Recovery Services Vault</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56cc3-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="56cc3-121">-Confirm</span></span>
<span data-ttu-id="56cc3-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="56cc3-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56cc3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56cc3-123">-WhatIf</span></span>
<span data-ttu-id="56cc3-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="56cc3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56cc3-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="56cc3-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56cc3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56cc3-126">CommonParameters</span></span>
<span data-ttu-id="56cc3-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="56cc3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56cc3-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="56cc3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56cc3-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="56cc3-129">INPUTS</span></span>

### <span data-ttu-id="56cc3-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="56cc3-130">None</span></span>

## <span data-ttu-id="56cc3-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="56cc3-131">OUTPUTS</span></span>

### <span data-ttu-id="56cc3-132">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="56cc3-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="56cc3-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="56cc3-133">NOTES</span></span>

## <span data-ttu-id="56cc3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="56cc3-134">RELATED LINKS</span></span>

[<span data-ttu-id="56cc3-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="56cc3-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="56cc3-136">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="56cc3-136">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="56cc3-137">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="56cc3-137">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


