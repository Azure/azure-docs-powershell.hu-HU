---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: c5ab79ca42096ab93102be1288c772cab1ac01f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679372"
---
# <span data-ttu-id="af53a-101">Unregister-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="af53a-101">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="af53a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af53a-102">SYNOPSIS</span></span>
<span data-ttu-id="af53a-103">Windows-kiszolgáló vagy más tároló regisztrációjának megszüntetése a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="af53a-103">Unregisters a Windows Server or other container from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af53a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af53a-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af53a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="af53a-105">DESCRIPTION</span></span>
<span data-ttu-id="af53a-106">A **unregister-AzureRmRecoveryServicesBackupContainer** parancsmag a Windows Server vagy más biztonsági tárolók nyilvántartását a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="af53a-106">The **Unregister-AzureRmRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="af53a-107">Ez a parancsmag eltávolítja a tárolóra mutató hivatkozást a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="af53a-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="af53a-108">A tároló törlése előtt törölnie kell az adott tárolóhoz társított összes védett adatot.</span><span class="sxs-lookup"><span data-stu-id="af53a-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="af53a-109">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="af53a-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="af53a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="af53a-110">EXAMPLES</span></span>

### <span data-ttu-id="af53a-111">1. példa: Windows-kiszolgáló regisztrációjának megszüntetése a boltozatról</span><span class="sxs-lookup"><span data-stu-id="af53a-111">Example 1: Unregister a Windows Server from the vault</span></span>
```
PS C:\>$Cont = Get-AzureRmRecoveryServicesContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="af53a-112">Az első parancs beolvassa a server01.contoso.com nevű Windows-tárolót, amely a boltozatban van regisztrálva, majd a $Cont változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="af53a-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>

<span data-ttu-id="af53a-113">A második parancs az Azure Backup Vault-ról regisztrálja a megadott Windows Servert.</span><span class="sxs-lookup"><span data-stu-id="af53a-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

## <span data-ttu-id="af53a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af53a-114">PARAMETERS</span></span>

### <span data-ttu-id="af53a-115">-Container</span><span class="sxs-lookup"><span data-stu-id="af53a-115">-Container</span></span>
<span data-ttu-id="af53a-116">Egy tartalék tároló objektumot ad meg a regisztráció törléséhez.</span><span class="sxs-lookup"><span data-stu-id="af53a-116">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="af53a-117">**BackupContainer** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="af53a-117">To obtain a **BackupContainer** object, use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af53a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af53a-118">-DefaultProfile</span></span>
<span data-ttu-id="af53a-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af53a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af53a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af53a-120">CommonParameters</span></span>
<span data-ttu-id="af53a-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af53a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af53a-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af53a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af53a-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af53a-123">INPUTS</span></span>

## <span data-ttu-id="af53a-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af53a-124">OUTPUTS</span></span>

## <span data-ttu-id="af53a-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af53a-125">NOTES</span></span>

## <span data-ttu-id="af53a-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af53a-126">RELATED LINKS</span></span>

[<span data-ttu-id="af53a-127">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="af53a-127">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)


